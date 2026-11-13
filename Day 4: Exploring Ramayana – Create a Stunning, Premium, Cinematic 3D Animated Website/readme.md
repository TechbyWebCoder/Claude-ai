# The Complete AI Prompt Guide: Ramayana Cinematic 3D Website

Ready-to-use master prompt + step-by-step build manual.

> *"The Eternal Epic. The Greatest Story Ever Told."*

**HTML5 · CSS3 · JavaScript · Three.js · GSAP**

Created by **TechByWebCoder**

© 2026 TechByWebCoder. All rights reserved. For personal and educational use.

---

## Table of Contents

| Part | Contents |
|------|----------|
| 1 | About this guide, tech stack, requirements |
| 2 | Step-by-step guide (8 steps from setup to publishing) |
| 3 | The Master Prompt: copy-ready, sectioned |
| 4 | Modular build strategy and follow-up refinement prompts |
| 5 | Troubleshooting, content and legal notes, final checklist |

---

## Part 1: About This Guide

This guide turns one detailed AI prompt into a complete, working Ramayana-inspired cinematic 3D website. You paste the master prompt into an AI assistant, save the generated code as a single `index.html`, and open it in your browser. No frameworks or build tools are needed. Everything loads from CDN links.

> **Quick start in 60 seconds**
> 1. Copy the Master Prompt from Part 3.
> 2. Paste it into your AI assistant.
> 3. Copy the generated code into `index.html`.
> 4. Open it with Live Server.
> 5. Refine with the follow-up prompts in Part 4.

### What You Will Build

| Layer | Technology | Purpose |
|-------|------------|---------|
| Structure | HTML5 | Single-page layout: hero, story, characters, gallery, movie info, footer |
| Styling | CSS3 | Dark-gold theme, glassmorphism, responsive grid, keyframe animations |
| Logic | JavaScript | Loader, custom cursor, lightbox, carousel, sound toggle, mobile menu |
| 3D / WebGL | Three.js | Forest scene, silhouette, particles, embers, fog, light rays, camera moves |
| Animation | GSAP + ScrollTrigger | Scroll-driven cinematic transitions, text reveals, parallax |
| Icons | Font Awesome (CDN) | Navigation, social links, buttons |

### Before You Start

- **Browser:** latest Chrome, Edge or Firefox with hardware acceleration ON (needed for WebGL).
- **Editor:** Visual Studio Code (free) with the Live Server extension.
- **Internet:** required, because Three.js, GSAP and icons load from CDNs.
- **AI assistant:** any model that can output long code (a full cinematic page is several thousand lines of tokens).

---

## Part 2: Step-by-Step Guide

### Step 01: Choose Your AI Assistant

- Pick an AI model that supports long outputs (Claude, ChatGPT, Gemini or similar).
- Start a fresh chat so older instructions do not interfere.
- If your tool offers an artifact, canvas or preview mode, switch it on to see the page live.

### Step 02: Set Up Your Workspace

- Install VS Code and add the Live Server extension.
- Create a folder named `ramayana-website` and an empty `index.html` inside it.
- Check that browser hardware acceleration is enabled (Settings > System).

### Step 03: Copy the Master Prompt

- Go to Part 3 and copy every section, from the opening line to the Final Deliverable line.
- Optional tweaks: palette, section names, number of story chapters, ambient sound on/off.
- Do not add invented release dates, cast or crew. Keep *Coming Soon* unless you have official sources.

### Step 04: Paste and Generate

- Paste the prompt into the AI chat and send it. Ask for one complete code block for `index.html`.
- If the reply stops midway, send: `Continue exactly from where you stopped. Do not repeat earlier code.`
- If it is still incomplete, switch to the Modular Strategy in Part 4 (build in 4 passes).

### Step 05: Save the Code as index.html

- Copy the full code block, paste it into `index.html` and press `Ctrl + S`.
- Make sure the file starts with `<!DOCTYPE html>` and ends with `</html>`.
- Keep the file encoding as UTF-8.

### Step 06: Run It in the Browser

- In VS Code: right-click `index.html` and choose **Open with Live Server**.
- No Live Server? Open a terminal in the folder, run the command below, and visit `http://localhost:8000`.
- Press `F12` and open the Console tab to spot any errors.

```bash
python -m http.server 8000
```

### Step 07: Test and Refine

- Check: loading screen, hero animation, smooth scroll, progress bar, tilt cards, lightbox, custom cursor, sound toggle (OFF by default).
- Press `Ctrl + Shift + M` in DevTools to test phone and tablet layouts.
- Change one thing per prompt and paste exact error messages. Use the follow-up prompts in Part 4.

### Step 08: Optimize and Publish

- Compress images (WebP), cap the renderer pixel ratio and reduce particle counts on mobile.
- Run Lighthouse (Chrome DevTools) to check performance and accessibility.
- Publish free on Netlify, GitHub Pages, Vercel or Cloudflare Pages. Credit all image sources.

---

## Part 3: The Master Prompt

Copy everything inside the code block. The prompt is split into labeled sections for readability. Paste them together as one prompt.

```text
[ OPENING ]
Create a stunning, premium, cinematic 3D animated website inspired by the upcoming RAMAYANA
movie. Build a fully responsive, visually immersive webpage using HTML5, CSS3, JavaScript,
Three.js, and GSAP animations.

WEBSITE THEME: Design a breathtaking mythological cinematic experience inspired by the Indian
epic Ramayana, featuring a dark golden, saffron, deep-red, and royal-blue color palette.

[ 1. HERO SECTION - CINEMATIC EXPERIENCE ]
- Full-screen cinematic landing page.
- Display a massive 3D animated Lord Rama-inspired silhouette holding a divine bow.
- Add a beautiful animated forest environment with mountains, floating particles, glowing
  embers, and divine light rays.
- Create a dramatic animated title: RAMAYANA.
- Add tagline: "The Eternal Epic. The Greatest Story Ever Told."
- Include an animated "EXPLORE THE EPIC" button.
- Add cinematic camera movement and parallax scrolling.

[ 2. 3D ANIMATION & VISUAL EFFECTS ]
Use Three.js and WebGL to create:
- Interactive 3D environments.
- Floating particles and magical golden dust.
- Dynamic lighting and realistic shadows.
- Animated clouds, fog, fire, and glowing energy effects.
- Smooth 3D camera transitions.
- Scroll-triggered cinematic animations.
- Depth-of-field and atmospheric effects.

[ 3. STORY SECTION ]
Create an interactive storytelling section featuring:
- The Birth of Lord Rama.
- Sita Swayamvar.
- The Exile of Rama.
- The Abduction of Sita.
- Hanuman's Journey to Lanka.
- The Battle of Lanka.
- The Victory of Dharma.
Use cinematic images, animated timelines, and smooth transitions.

[ 4. CHARACTER SHOWCASE ]
Create premium interactive 3D character cards for: Lord Rama, Goddess Sita, Lakshmana, Hanuman,
Ravana, King Dasharatha.
Each card should include character artwork, name, short description, hover effects, and 3D tilt
animations.

[ 5. CINEMATIC GALLERY ]
- Full-width cinematic movie-inspired visuals.
- Animated image carousel.
- Smooth zoom-in and transition effects.
- Interactive gallery with lightbox functionality.

[ 6. MOVIE INFORMATION ]
Create a professional movie information section with:
- Movie title and cinematic poster.
- Release information (only verified information; otherwise display "Coming Soon").
- Cast and production information (avoid inventing details).
- An animated "WATCH TRAILER" button with a placeholder if no official trailer is available.

[ 7. ADDITIONAL FEATURES ]
- Premium animated navigation bar.
- Custom animated cursor.
- Loading screen with a glowing Ramayana logo.
- Smooth scrolling.
- Responsive mobile navigation.
- Scroll progress indicator.
- Animated footer with social media links.
- Background ambient sound toggle (off by default).

[ 8. TECHNICAL REQUIREMENTS ]
- HTML5, CSS3, JavaScript.
- Three.js for 3D environments and models.
- GSAP + ScrollTrigger for cinematic animations.
- Use Font Awesome or Lucide icons.
- Use modern CSS animations, gradients, glassmorphism, and responsive layouts.
- Optimize 3D rendering for desktop and mobile.
- Add fallback visuals if WebGL is unavailable.
- Write clean, modular, well-commented code.

[ 9. DESIGN DIRECTION ]
Reference aesthetic: Hollywood-level cinematic presentation mixed with Indian mythology,
premium movie promotional websites, realistic 3D environments, dramatic lighting, and elegant
typography.

IMPORTANT: Do not create a basic template or ordinary static landing page. Make it feel like an
actual high-budget Indian mythological movie website. Every section should have impressive
visual storytelling, smooth animations, cinematic transitions, and interactive elements.

[ FINAL DELIVERABLE ]
Generate a complete, functional, single-page index.html file with embedded CSS and JavaScript
wherever practical. Include all required dependencies through CDN links. The website must run
directly in a modern browser.
```

---

## Part 4: Modular Strategy and Follow-Up Prompts

### Why build in passes?

AI tools have an output limit. A full cinematic page can exceed it, so the reply may stop early or lose quality at the end. If that happens, use the same Master Prompt but ask for the work in four passes, then merge the results into one `index.html`.

| Pass | Ask the AI to build | Result |
|------|---------------------|--------|
| A | Loading screen, navigation, scroll progress, custom cursor, and the full Hero with the Three.js scene | Working base page with 3D hero |
| B | Story timeline (7 chapters) and 6 character cards with 3D tilt | Content sections added |
| C | Gallery carousel + lightbox, Movie Information section, animated footer, sound toggle | Remaining sections added |
| D | Polish: mobile optimization, WebGL fallback, performance, accessibility, comments | Final production file |

**Pass instruction to add each time**

```text
Return the FULL updated index.html every time, not snippets. Keep all earlier
features working. Use the same CSS variables and file structure.
```

### Follow-Up Refinement Prompts

**Continue a cut-off reply**

```text
Continue exactly from where you stopped. Do not repeat earlier code.
```

**Fix an error**

```text
I get this console error: [paste exact error]. Find the cause and return the
corrected full file.
```

**Mobile performance**

```text
Optimize for mobile: cap renderer pixel ratio at 1.5, reduce particles by 60%,
disable shadows and heavy post-processing under 768px.
```

**More cinematic hero**

```text
Improve the hero: slower camera dolly, stronger volumetric light rays, layered
fog, and a smoother title reveal with GSAP.
```

**Add real 3D models**

```text
Add a GLTFLoader that loads ./assets/rama.glb if present, otherwise falls back
to the procedural silhouette.
```

**Accessibility**

```text
Add prefers-reduced-motion support, keyboard focus styles, alt text, and ARIA
labels without changing the visuals.
```

**Split into files**

```text
Refactor into index.html, style.css and main.js with clean modules and
comments. Keep behaviour identical.
```

---

## Part 5: Troubleshooting, Notes and Final Checklist

### Common Problems and Fixes

| Problem | Likely cause | Fix |
|---------|--------------|-----|
| Black or empty 3D scene | WebGL disabled, or Three.js CDN blocked | Enable hardware acceleration; check Console and network; ensure the script tag loads before your code. |
| Scroll animations do nothing | ScrollTrigger plugin not registered | Confirm `gsap.registerPlugin(ScrollTrigger)` runs after both scripts load. |
| Textures or audio fail to load | Opened as `file://` with local assets | Run through Live Server or `python -m http.server`. |
| Ambient sound will not play | Browsers block autoplay | Expected. Sound starts OFF and plays only after the user clicks the toggle. |
| Page lags on phones | Too many particles or shadows | Use the Mobile performance prompt from Part 4. |
| Custom cursor looks wrong on touch | No mouse on mobile | Hide the custom cursor on touch devices (`pointer: coarse`). |

### Content, Accuracy and Legal Notes

- **Movie facts:** publish only information confirmed by official announcements. Otherwise show *Coming Soon* and *To Be Announced*. Never invent dates, cast or crew.
- **Artwork:** use original, AI-generated or properly licensed images. Do not copy posters, stills or trailers you do not own.
- **Trailer:** keep the placeholder until an official trailer link exists, then embed that official link.
- **Respect:** the Ramayana is sacred to millions. Keep the portrayal dignified.
- **Independent project:** this is a fan-made, inspiration-based page and is not affiliated with the film's producers.

### Final Launch Checklist

- [ ] Loader shows glowing logo, then reveals the hero
- [ ] RAMAYANA title and tagline animate correctly
- [ ] 3D scene runs smoothly; fallback works with WebGL off
- [ ] All 7 story chapters and 6 character cards present
- [ ] Tilt effects, lightbox and carousel work
- [ ] Movie info shows only verified details or Coming Soon
- [ ] Navigation, progress bar and mobile menu work
- [ ] Ambient sound is OFF by default and toggles properly
- [ ] No console errors; Lighthouse score checked
- [ ] Image credits added; site published

---

**Created by TechByWebCoder**

Thank you for using this guide. Keep experimenting, keep building, and keep your code clean. Share your finished Ramayana experience and credit your sources.
