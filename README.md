# Gen AI Portfolio

Three small AI-powered tools, each built from scratch to learn generative AI hands-on while transitioning into technical project management roles.

**Live site:** https://bezetam.github.io/ai-projects/portfolio.html

## Projects

### 1. PRD → Tasks
Paste a product requirements doc, get back a prioritized, estimated task list broken out by team (Engineering, Design, PM). Switches between the Gemini and Claude APIs from the same interface, with CSV export.

**Stack:** Vanilla JS · Claude API · Gemini API · localStorage
**File:** [`prd-to-tasks-v4.html`](./prd-to-tasks-v4.html)

### 2. Meeting Summarizer
Paste a standup or meeting transcript, get back a plain-English summary, an action-item list with owners and due dates, and a log of decisions made — three different output shapes from a single prompt.

**Stack:** Vanilla JS · Gemini API
**File:** [`meeting-summarizer.html`](./meeting-summarizer.html)

### 3. Project Estimator
Estimates project scope and timeline using a locally-run DeepSeek R1 model (via LM Studio) grounded with live web search — no cloud API costs, runs entirely on-device.

**Stack:** Python · Streamlit · LM Studio · DeepSeek R1
**Note:** requires a local LM Studio setup to run; not hosted here.

## What this demonstrates

- Prompt engineering for structured JSON output
- Multi-provider API integration (Claude + Gemini)
- Local LLM inference vs. cloud API tradeoffs
- Async/await, error handling, and empty-state design
- Client-side data persistence

## Running the HTML projects locally

Each `.html` file is self-contained — download it, open it in any browser, and paste in your own API key (Gemini keys are free at [aistudio.google.com](https://aistudio.google.com/app/apikey)).

---

Built by Alan Bezet — https://www.linkedin.com/in/alanbezet/ - alan.bezet@gmail.com 