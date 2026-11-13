# GitHub Profile: Steps + AI Prompt

**TechbyWebCoder // GitHub Profile Setup Instructions + Prompt**

[techbywebcoder.netlify.app](https://techbywebcoder.netlify.app) | [github.com/TechbyWebCoder](https://github.com/TechbyWebCoder)

> ARC REACTOR: ONLINE
> SUIT UPGRADE: IN PROGRESS

**Full Stack Developer: GitHub Profile, Steps + AI Prompt**

Step-by-step instructions + one ready-to-use AI prompt. Beginner friendly. Web + Git methods. 1 AI prompt.

---

## 01. Before You Start

A GitHub profile README is a special repository that appears at the top of your public profile. GitHub shows it automatically when a repository has the same name as your username.

| Step | What to do | Result |
|------|------------|--------|
| 01 | **Create a repo** named exactly like your username | Special profile repository |
| 02 | **Add README.md** and make the repo Public | Content ready |
| 03 | **Live on profile** | GitHub shows it at the top of your page |

### What you need

- A free GitHub account and a modern web browser. That is enough for the web method.
- Optional: Git and VS Code installed, for the local method.
- Your details ready: bio, tech stack, top repositories and social links.
- An AI assistant (ChatGPT, Claude, Gemini or Grok) to run the prompt in section 04.

> **Good to know: no custom CSS or JavaScript.**
> GitHub strips custom CSS and JavaScript from READMEs, so the prompt in section 04 asks the AI for Markdown and basic HTML only.

---

## 02. Setup on GitHub.com (Web Method)

### 1. Sign in and polish your account

Log in at github.com. Open **Settings → Public profile** and add a profile photo, your name, a short bio and your location. A complete profile makes the README look far better.

### 2. Create the special repository

Click the **+** icon (top-right) → **New repository**, or open [github.com/new](https://github.com/new).

- Repository name must match your GitHub username exactly, e.g. `TechbyWebCoder`.
- GitHub then shows a notice that this is a special repository whose README appears on your profile.
- Set visibility to **Public**.
- Tick **Add a README file**.
- Click **Create repository**.

### 3. Open README.md in the editor

Inside the new repository click `README.md`, then the pencil icon (**Edit this file**). The built-in editor opens with a Preview option so you can check your work.

### 4. Add your profile content

Delete the starter text and paste your own README. Build it in this order: banner and role line, whoami block, tech loadout badges, projects table, mission log, social links, closing quote. The easiest way: run the AI prompt in section 04 and paste the README it writes for you.

### 5. Preview before you save

Use the Preview option and check that every badge, banner and image loads and that each link opens the right page. Broken pictures nearly always mean a typo in the image URL.

### 6. Commit your changes

Click the green **Commit changes...** button, write a message such as `Update profile README`, keep **Commit directly to the main branch** selected, then click **Commit changes**.

### 7. View your live profile

Open `github.com/YOUR-USERNAME`. Your README appears at the top of the Overview tab. If it looks stale, hard-refresh with `Ctrl + F5` or `Cmd + Shift + R` and wait a minute.

### 8. Pin your best repositories

On your profile click **Customize your pins**, tick up to 6 repositories you want visitors to see first, then click **Save pins**.

---

## 03. Setup with Git + VS Code

Prefer to work locally? Use this method. It is the same result, edited on your computer and pushed to GitHub.

### 1. Install Git and VS Code

Download Git from [git-scm.com](https://git-scm.com) and VS Code from [code.visualstudio.com](https://code.visualstudio.com). Both are free. Restart your terminal after installing.

### 2. Tell Git who you are (one time only)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### 3. Clone your profile repository

Create the repo as in section 02 (steps 1-2), then run:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-USERNAME.git
cd YOUR-USERNAME
code .
```

### 4. Edit README.md in VS Code

Make your changes and save. Press `Ctrl + Shift + V` to open the live Markdown preview beside the editor.

### 5. Commit and push

```bash
git add README.md
git commit -m "Update profile README"
git push origin main
```

> If Git asks you to sign in, use the browser sign-in (Git Credential Manager) or a Personal Access Token. GitHub no longer accepts your account password for Git over HTTPS.

> New repositories use `main` by default. If `git branch` shows a different branch name, use that name in the push command.

---

## 04. The AI Prompt

Copy the prompt below into ChatGPT, Claude, Gemini or Grok. Replace every `[bracket]` with your own details, then paste the README it writes into your repository (section 02, step 4).

**PROMPT // Profile README generator**

```text
ROLE
You are a senior developer-advocate and GitHub profile designer.

TASK
Create a complete GitHub profile README.md in an "Iron Man" theme
(red and gold armour, cyan arc-reactor accents, dark tech feel).

MY DETAILS (replace everything in [brackets])
- GitHub username: [YOUR-USERNAME]
- Display name: [YOUR NAME]
- Role / title: [e.g. Aspiring Full Stack Developer]
- Location: [CITY, COUNTRY]
- Currently learning: [TOPICS]
- Goal: [YOUR GOAL]
- Fun fact: [ONE LINE]
- Tech stack: [languages, frontend, backend, databases, tools]
- Top repositories: [name - one-line description - language - stars] (up to 6)
- Social links: [GitHub, Instagram, YouTube, Telegram, website]

THEME RULES
- Palette: red #D7262E, deep red #8F111A, gold #F5C04A, arc cyan #7BE7FF, void #080304.
- Use ONLY what a GitHub README supports: Markdown plus basic HTML
  (div/p align, img, picture, a, table, details). No CSS, no JavaScript.
- Banner: capsule-render waving banner (solid colour 8F111A, gold text).
- Typing line: readme-typing-svg in cyan 7BE7FF using my role lines.
- Tech badges: shields.io "for-the-badge" style with simple-icons logos.

SECTIONS (in this order)
1. Banner + typing line + short status line
2. whoami - my profile as a JavaScript object in a js code block
3. Tech loadout - badges grouped as Frontend / Languages / Databases / Tools
4. Projects table - Repository | What's inside | Language | Stars (linked)
5. Mission log - 5 to 6 goals as a checklist
6. GitHub stats card using the palette colours (optional block)
7. Connect with me - social badges with links
8. Footer - one dev quote + a "drop a star" line

OUTPUT FORMAT
- Return ONE copy-paste-ready README.md inside a single markdown code block.
- Build every URL correctly for my username. Do not invent repositories.
- After the code block, add 3 bullets: what I must change, and anything
  that may fail to load.
```

### After you get the result

Copy the README.md code block the AI returns, paste it into `README.md`, check the Preview, fix anything the AI flagged in its 3 closing bullets, then commit.
