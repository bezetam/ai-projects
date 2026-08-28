# Gen AI Portfolio

Five small AI-powered tools, each built from scratch to learn generative AI hands-on while transitioning into technical project management roles.

**Live site:** https://bezetam.github.io/ai-projects/portfolio.html

## Projects

### 1. PRD → Tasks

Paste a product requirements doc, get back a prioritized, estimated task list broken out by team (Engineering, Design, PM). Switches between the Gemini and Claude APIs from the same interface, with CSV export.

**Stack:** Vanilla JS · Claude API · Gemini API · localStorage
**File:** `prd-to-tasks-v4.html`

### 2. Meeting Summarizer

Paste a standup or meeting transcript, get back a plain-English summary, an action-item list with owners and due dates, and a log of decisions made — three different output shapes from a single prompt.

**Stack:** Vanilla JS · Gemini API
**File:** `meeting-summarizer.html`

### 3. Project Estimator

Estimates project scope and timeline using a locally-run DeepSeek R1 model (via LM Studio) grounded with live web search — no cloud API costs, runs entirely on-device.

**Stack:** Python · Streamlit · LM Studio · DeepSeek R1
**Note:** requires a local LM Studio setup to run; not hosted here.

### 4. Release Notes Agent

Paste raw ticket/release data, get back three tailored release notes generated from the same source — technical detail for engineering, plain language for customers, business impact for leadership. Switches between the Gemini and Claude APIs from the same interface, with sample data pre-filled so it's usable immediately.

**Stack:** Vanilla JS · Claude API · Gemini API
**File:** `release-notes-demo.html`
**Also available as:** a standalone Python CLI at [github.com/bezetam/release-notes-agent](https://github.com/bezetam/release-notes-agent), which adds a deterministic template fallback for when no API key is set.

### 5. Program Status Rollup Agent

Paste in raw sprint updates for every team on a program, get back a single leadership-ready status. One agent pass reads each team's notes and returns a status rating with specific risks; a second pass reads all the team summaries together and produces one program-level status, surfacing cross-team dependencies that no individual team's report would show on its own. Supports a bulk-paste format for swapping in a whole new dataset at once.

**Stack:** Vanilla JS · Claude API · Gemini API
**File:** `program-status-rollup-demo.html`

## What this demonstrates

* Prompt engineering for structured JSON and audience-adaptive text output
* Multi-provider API integration (Claude + Gemini)
* Multi-step agent orchestration, chaining one agent's output into a second agent's input
* Local LLM inference vs. cloud API tradeoffs
* Async/await, error handling, and empty-state design
* Client-side data persistence
* Iterating on prompts against real output rather than stopping at the first working version

## Running the HTML projects locally

Each `.html` file is self-contained — download it, open it in any browser, and paste in your own API key (Gemini keys are free at [aistudio.google.com](https://aistudio.google.com/app/apikey)). Keep all five HTML files in the same folder — `portfolio.html`'s project links are relative paths, so they'll 404 if moved apart.

Built by Alan Bezet — https://www.linkedin.com/in/alanbezet/ · [alan.bezet@gmail.com](mailto:alan.bezet@gmail.com)
