# 8 Free AI Skills for Students & Job Seekers

From **[@develop.with.guna](https://www.instagram.com/develop.with.guna/)**: study smarter, build better projects, and land the job, using free skills for Claude.

> **What's a skill?** It's like a recipe card for AI. You give it to Claude once, and Claude knows how to do that job properly every time.

| # | Skill | What it does for you | Claude app | Claude Code |
|---|-------|----------------------|:---:|:---:|
| 1 | [Teach Me](#1-teach-me) | A tutor that asks you questions until you really understand | ✅ upload | ✅ |
| 2 | [Exam](#2-exam) | Turns your notes into flashcards, practice questions and mock tests | ✅ upload | ✅ |
| 3 | [Superpowers](#3-superpowers) | Makes Claude plan, build and test your project like a real dev team | ❌ | ✅ |
| 4 | [Frontend Design](#4-frontend-design) | Builds a portfolio website that doesn't look AI-made | ✅ upload | ✅ |
| 5 | [PDF & Word](#5-pdf--word) | Makes your resume a clean, ready-to-send PDF or Word file | ✅ built in | ✅ |
| 6 | [Job Seeker Skills](#6-job-seeker-skills) | Tailors your resume to a job post, writes the cover letter, preps your interview | ✅ upload | ✅ |
| 7 | [Career Ops](#7-career-ops) | Scores how well you fit a job before you apply | ❌ | ✅ |
| 8 | [Skill Creator](#8-skill-creator) | Describe a skill you need, and Claude builds it | ✅ built in | ✅ |

**Not a coder?** Use the **Claude app** (claude.ai or the phone/desktop app). Skills 1, 2, 4, 5, 6 and 8 work there.
**Comfortable with a terminal?** Use **Claude Code**. All 8 work there.

---

## First, the two ways to add a skill

### A. In the Claude app (no coding)
Skills work on the Free, Pro, Max, Team and Enterprise plans.

1. Go to **Settings → Capabilities** and turn on **Code execution and file creation**.
2. **Built-in skills** (PDF, Word, Skill Creator): go to **Customize → Skills** and switch them on. That's it.
3. **Skills from GitHub**: you upload them as a ZIP.
   1. Open the skill's GitHub link below → green **Code** button → **Download ZIP** → unzip it.
   2. Find the skill's folder (the one with `SKILL.md` inside) and zip **just that folder**.
   3. In Claude, go to **Customize → Skills → + → Create skill → Upload a skill**, and pick your ZIP.
   4. Switch it on, then start a new chat.

### B. In Claude Code (terminal)
You need [Claude Code](https://claude.com/claude-code) installed. Skills live in a folder:
- Windows: `C:\Users\<you>\.claude\skills\`
- Mac / Linux: `~/.claude/skills/`

Each skill below has the exact command. Restart Claude Code after installing, then type `/` to see your skills.

---

## 1. Teach Me
**A private tutor that makes *you* do the thinking.** It builds a learning plan, asks you questions (instead of just giving answers), uses spaced repetition, and makes a lesson page for each session.

- Source: [citypaul/.dotfiles → teach-me](https://github.com/citypaul/.dotfiles/tree/main/claude/.claude/skills/teach-me)
- Claude Code:
  ```bash
  npx skills add https://github.com/citypaul/.dotfiles --skill teach-me
  ```
- Claude app: download the repo ZIP and upload the `claude/.claude/skills/teach-me` folder (see A.3).
- Try it: `/teach-me recursion in Python`

## 2. Exam
**Exam prep from your own notes.** Practice questions (MCQ, short answer, essay), flashcards, timed mock exams, a study schedule for your exam date, and a list of your weak topics.

- Source: [satoshistackalotto/skills → exam](https://github.com/satoshistackalotto/skills/tree/main/skills/ivangdavila/exam) (MIT)
- Claude Code (Windows PowerShell):
  ```powershell
  mkdir $HOME\.claude\skills\exam -Force
  curl.exe -L https://raw.githubusercontent.com/satoshistackalotto/skills/HEAD/skills/ivangdavila/exam/SKILL.md -o $HOME\.claude\skills\exam\SKILL.md
  ```
- Claude Code (Mac / Linux):
  ```bash
  mkdir -p ~/.claude/skills/exam
  curl -L https://raw.githubusercontent.com/satoshistackalotto/skills/HEAD/skills/ivangdavila/exam/SKILL.md -o ~/.claude/skills/exam/SKILL.md
  ```
- Claude app: put that `SKILL.md` in a folder called `exam`, zip the folder and upload it (see A.3).
- Try it: attach your unit notes and say *"Make 10 practice questions and flashcards from this. My exam is on 15 Nov."*

## 3. Superpowers
**Build your college project the way real dev teams do.** Claude brainstorms with you first, writes a plan, builds step by step, tests, debugs properly, and checks the work before saying "done".

- Source: [obra/superpowers](https://github.com/obra/superpowers) (MIT)
- Claude Code: type these inside Claude Code:
  ```text
  /plugin install superpowers@claude-plugins-official
  ```
- Try it: *"I want to build an attendance app for my final-year project. Help me plan it."*

## 4. Frontend Design
**A portfolio website that looks designed, not AI-generated.** Bold, unique layouts and fonts instead of the usual purple-gradient template.

- Source: [anthropics/skills → frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) (official, by Anthropic)
- Claude Code:
  ```text
  /plugin marketplace add anthropics/skills
  /plugin install example-skills@anthropic-agent-skills
  ```
- Claude app: download the repo ZIP and upload the `skills/frontend-design` folder (see A.3).
- Try it: paste your resume and say *"Build me a one-page portfolio website from this."*

## 5. PDF & Word
**Your resume as a clean, ready-to-send file.** Also makes Word docs, PowerPoint slides and Excel sheets for college work.

- Source: [anthropics/skills → pdf](https://github.com/anthropics/skills/tree/main/skills/pdf), [docx](https://github.com/anthropics/skills/tree/main/skills/docx) (official, by Anthropic)
- Claude app: **already built in.** Turn on *Code execution and file creation* (see A.1), and Claude uses it automatically.
- Claude Code:
  ```text
  /plugin marketplace add anthropics/skills
  /plugin install document-skills@anthropic-agent-skills
  ```
- Try it: *"Turn my resume into a clean one-page PDF."*

## 6. Job Seeker Skills
**Your job application kit.** Paste a job post + your resume and get a tailored resume, cover letter, recruiter message, interview prep and a tracker. It's built **not** to invent experience you don't have.

- Source: [Faizee-Asad/job-seeker-claude-skills](https://github.com/Faizee-Asad/job-seeker-claude-skills) (MIT)
- Claude app: upload the `.claude/skills/job-seeker-helper` folder first (see A.3). Add the others (`resume-optimizer`, `cover-letter`, `interview-coach`, `job-application-tracker`) if you want them.
- Claude Code:
  ```bash
  git clone https://github.com/Faizee-Asad/job-seeker-claude-skills.git
  mkdir -p ~/.claude/skills
  cp -R job-seeker-claude-skills/.claude/skills/* ~/.claude/skills/
  ```
- Try it: `/job-seeker-helper` and paste the job description + your resume.

## 7. Career Ops
**A full job-search system.** Paste a job link and it scores your fit (1 to 5) against your CV, then makes a tailored resume PDF, a cover letter, interview prep, and keeps a tracker. It never applies for you; you press Submit.

- Source: [career-ops-hq/career-ops](https://github.com/career-ops-hq/career-ops) (MIT)
- Needs [Node.js](https://nodejs.org). Then:
  ```bash
  npx @santifer/career-ops init
  ```
  Open the folder it creates, run `claude`, and it walks you through setup in chat.
- Try it: paste a job URL and let it evaluate.

## 8. Skill Creator
**Can't find the skill you need? Make your own.** Describe what you want in plain words, and Claude writes the skill for you.

- Source: [anthropics/skills → skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) (official, by Anthropic)
- Claude app: **Customize → Skills** → switch on *skill-creator*.
- Claude Code: comes with `example-skills` (same commands as #4).
- Try it: *"Make a skill that turns my class notes into 5 viva questions."*

---

## Safety tips
- **Read before you install.** A skill is just a text file (`SKILL.md`). Open it and see what it asks Claude to do.
- **Check what it writes.** AI can be wrong. Read your resume and cover letter before sending them.
- **Never let a tool lie for you.** Only real skills and real projects on your resume.

## Credits
All skills belong to their authors and keep their own licences. This repo only links to them; nothing is copied here.
Teach Me by [citypaul](https://github.com/citypaul) · Exam by ivangdavila (via [satoshistackalotto/skills](https://github.com/satoshistackalotto/skills)) · Superpowers by [obra](https://github.com/obra) · Frontend Design, PDF/Word, Skill Creator by [Anthropic](https://github.com/anthropics/skills) · Job Seeker Skills by [Faizee-Asad](https://github.com/Faizee-Asad) · Career Ops by [career-ops-hq](https://github.com/career-ops-hq).

---

Made with 💚 by **Gunasekaran R** · Follow [@develop.with.guna](https://www.instagram.com/develop.with.guna/) for more tools like this.
