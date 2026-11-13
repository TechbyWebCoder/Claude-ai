# Turn a Video into a 2D Rock-Themed Animation

Tutorial from this chat, plus a ready-to-paste prompt. Result: one self-contained HTML file with synced audio.

---

## 1. What we built

You uploaded a 22.7-second portrait video (720 x 1280, 25 fps) of a singer in profile at a microphone. Claude redrew him as a flat 2D cartoon on an HTML5 canvas, put him on a rock stage, and kept the original audio. His mouth, head, hair, the lights and the lightning all react to how loud the song is at each moment.

---

## 2. The workflow, step by step

1. **Inspect the video.** Claude ran `ffprobe` to read duration, size, frame rate and codecs (H.264 video, AAC audio).
2. **Look at the frames.** `ffmpeg` pulled one frame every 4 seconds into a contact sheet. This showed the subject: black cap with orange stitching, sunglasses, locs, beard, white tee, green curtain, microphone on the left.
3. **Extract the audio.** The soundtrack became a small mono MP3 (about 160 KB) so it can live inside the HTML file.
4. **Measure loudness.** The audio was decoded to 8 kHz mono, split into 40 ms windows, and the RMS level of each window was normalized to 0-1 and lightly smoothed. That gave 567 numbers, one per 40 ms.
5. **Design the scene.** Layers, back to front: dark red/purple gradient, sweeping spotlights, drifting embers, four amp stacks, lightning bolts, neon "ROCK" sign, the character, the mic, equalizer bars, vignette.
6. **Add the motion logic.** A fast and a slow moving average of the loudness are compared. When the fast one jumps above the slow one, a "kick" value spikes, then decays. Kick drives screen shake, light brightness, amp pulse, head bob and lightning.
7. **Embed everything.** The MP3 (base64) and the loudness array are written into the HTML, so there are no external files or libraries.
8. **Check and publish.** A syntax check (`node --check`) confirmed the script parses, then the page was published. Press Play to start, because browsers block autoplay with sound.

---

## 3. Key commands used

```bash
ffprobe -v error -show_entries format=duration:stream=codec_name,width,height video.mp4

ffmpeg -i video.mp4 -vf "fps=1/4,scale=240:-1,tile=6x1" -frames:v 1 sheet.jpg

ffmpeg -i video.mp4 -vn -ac 1 -ar 32000 -c:a libmp3lame -b:a 56k a.mp3

ffmpeg -i video.mp4 -vn -ac 1 -ar 8000 -f s16le -   # then RMS per 320 samples (40 ms)

node --check script.js   # syntax check of the embedded JavaScript
```

---

## 4. How the sync works

Every frame the page reads `audio.currentTime`, looks up the loudness at that time, and computes:

- **Mouth open** = loudness x a fast flutter
- **Kick** = how far loudness jumped above its recent average

Lightning fires when kick passes about 0.55, with a short cooldown. If the browser blocks audio, the animation falls back to a timer and still plays.

---

## 5. Limits to know

- The mouth follows loudness, not the actual words (no lip-reading).
- The character is a stylized redraw, not a frame-by-frame trace of the footage.
- In this chat the script was syntax-checked but not opened in a browser, so small visual details (face proportions, cap shape) may need tweaks. Ask for a screenshot pass and fixes if something looks off.
- Use only audio and footage you have the right to use.

---

## 6. The proper prompt (copy and paste)

Replace the `[BRACKETED]` parts with your own details. Upload the video in the same message.

```text
I am uploading a video (MP4). Convert it into ONE self-contained HTML file with a 2D
animation in a [ROCK / METAL / PUNK] theme.

Do this in order:

1. Inspect the video with ffprobe/ffmpeg: duration, resolution, fps, audio. Extract a
   few frames and describe the main subject (face, hair, hat, glasses, clothes, pose,
   props, background).

2. Extract the audio as a small mono MP3 (about 56 kbps). Compute a loudness envelope:
   RMS every 40 ms, normalized to 0-1 and lightly smoothed.

3. Redraw the main subject as a flat 2D vector character on an HTML5 canvas that
   matches the video's aspect ratio (for example 720x1280 for portrait). Keep these
   recognizable features: [HAT, SUNGLASSES, LOCS/HAIR, BEARD, CLOTHES].

4. Build the stage: dark red/purple gradient, sweeping spotlights, amp stacks that
   pulse, lightning on loud hits, rising embers, neon title text "[YOUR TITLE]",
   equalizer bars along the bottom, screen shake and a vignette.

5. Sync with audio.currentTime: drive mouth opening, head bob, hair sway, light
   brightness and lightning from the loudness envelope. Add a beat "kick" detector
   (fast average vs slow average).

6. Embed the MP3 as a base64 data URI and the envelope as an array inside the HTML.
   No external files, no libraries, no localStorage.

7. Add a big Play/Replay button (browsers block autoplay), a thin progress bar, and
   responsive scaling for phones. If audio fails to play, fall back to a timer.

8. Run a JavaScript syntax check, then open the page in a headless browser and take a
   screenshot. Fix anything that looks wrong (face proportions, overlapping shapes,
   text cut off). Then publish the page and give me the link plus the .html file.

Rules: keep the file under 1 MB, no copyrighted characters or logos, keep the
animation moving even when idle, and tell me in one line what you assumed.
```

### Short version

```text
Turn my uploaded video into a single HTML file with a 2D rock-themed animation. Redraw
the main subject as a flat vector character on a canvas, put him on a stage with
spotlights, amps, lightning and a neon title, keep the original audio embedded, and
sync mouth, head bob and lights to the audio loudness. Add a Play button, test it with
a screenshot, and publish it.
```

---

## 7. Ways to customize

- **Change the theme words:** "heavy metal with fire and skulls", "punk poster style", "retro 80s hair-metal neon".
- **Ask for a different art style:** "pixel art", "comic book halftone", "black and white woodcut".
- **Ask for extras:** guitar solo silhouette, crowd hands at the bottom, subtitles, or a download-as-video button.
- **For landscape videos,** tell Claude the canvas should be 1280x720 instead.
