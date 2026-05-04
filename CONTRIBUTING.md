# Contributing to AIUI

Thank you for your interest in contributing to AIUI.  
This project follows a strict architecture defined through OpenSpec files located in `/specs`.  
All code MUST follow these specifications.

---

## 🧠 1. Architecture Source of Truth

AIUI is fully defined by the OpenSpec modules in `/specs`.

- No feature may be implemented without a SPEC.
- No code may contradict a SPEC.
- If a SPEC is unclear, open an issue before coding.
- SPECs may only be modified through a dedicated PR and require human approval.

---

## 🌳 2. Branching Model

AIUI uses a structured Git workflow designed for human contributors and AI agents.

```
feature/*  →  dev  →  release  →  main
```


### ✔️ `feature/*` — Work branches  
Used by humans and AI agents.  
Free to break, rewrite, experiment.

Examples:
- feature/frontend-shell  
- feature/backend-storage  
- feature/agents-module  

### ✔️ `dev` — Integration branch  
Stable development branch.  
All features must be merged here via PR.

### ✔️ `release` — Pre-production  
Used to prepare stable versions.  
Only PRs from `dev`.

### ✔️ `main` — Production  
Only receives PRs from `release`.  
Fully protected.

---

## 🔀 3. How to Contribute Code

### Step 1 — Create a feature branch

```
git checkout -b feature/<name>
```


### Step 2 — Implement the feature following the SPECs
- Read the corresponding SPEC in `/specs`
- Follow types, routes, events, and rules exactly
- Do not invent APIs or structures not defined in SPECs

### Step 3 — Open a Pull Request into `dev`
Your PR must include:

- Summary of the change  
- SPECs referenced (e.g., “Implements 14-workspaces”)  
- Screenshots for UI changes  
- Notes for reviewers  

### Step 4 — Human or AI review  
PRs must be reviewed before merging.

### Step 5 — Merge into `dev`  
Only after review and checks.

---

## 🤖 4. AI Agent Contribution Rules

AI agents (Cline, Cursor, Windsurf, OpenCode) MUST:

- Read `/specs` before generating code  
- Follow the architecture strictly  
- Never modify SPECs unless explicitly instructed  
- Never push directly to `dev`, `release`, or `main`  
- Always work in `feature/*` branches  
- Always create PRs instead of direct commits  
- Never delete or rewrite protected branches  

Agents should include in PR description:

```
AI Agent: <name>
SPECs followed: <list>
Files modified: <list>
Reasoning summary: <short explanation>
```

---

## 📦 5. Project Structure

```
/app/frontend     → Angular 21 UI
/app/backend      → Node + TypeScript API
/app/src-tauri    → Tauri 2 desktop runtime
/shared           → Generated types from SPECs
/specs            → OpenSpec architecture (source of truth)
/web              → Public website (Astro)
```

---

## 🧪 6. Testing & Validation

Before submitting a PR:

- Ensure the app compiles  
- Ensure backend starts  
- Ensure Tauri builds (optional)  
- Ensure no SPEC violations  
- Ensure no unused files or dead code  

---

## 🐛 7. Reporting Bugs

Use the **Bug Report** template in `.github/ISSUE_TEMPLATE/`.

Include:

- Steps to reproduce  
- Expected behavior  
- Actual behavior  
- Logs or screenshots  
- SPECs affected  

---

## 💡 8. Requesting New Features

Use the **Feature Request** template.

Include:

- Motivation  
- SPEC impact  
- Proposed behavior  
- Optional diagrams  

---

## 📜 9. Code Style

- TypeScript strict mode  
- Angular standalone components  
- No magic strings  
- Use shared types from `/shared`  
- Follow naming conventions from SPECs  
- Keep modules isolated and clean  

---

## 🛡️ 10. Security

- Do not commit secrets  
- Do not bypass permission rules  
- Follow the security guidelines in SPEC 07  

---

Thank you for contributing to AIUI.  
This project is built on precision, clarity, and strong architectural foundations.  
Your contributions help keep it clean, scalable, and future-proof.
