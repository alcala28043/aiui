# Contributing to AIUI

Thank you for your interest in contributing!

## 📐 Architecture Source of Truth
All features, modules, routes, services, and types MUST follow the OpenSpec
definitions located in `/specs`.

No code should be added that contradicts or bypasses a SPEC.

## 🧱 Project Structure
- `/app/frontend` → Angular 21
- `/app/backend` → Node + TypeScript
- `/app/src-tauri` → Tauri 2 (Rust)
- `/shared` → Generated types from SPECs
- `/specs` → OpenSpec architecture (source of truth)
- `/web` → Public website

## 🔀 Branching Model
- `main` → stable, protected
- `dev` → active development
- feature branches → `feature/<name>`

## 🧪 Pull Requests
- Follow SPECs
- Include description of changes
- Include screenshots for UI changes
- No direct commits to `main`

## 🤖 AI Contributions
AI agents (Cline, Cursor, Windsurf, OpenCode) MUST:
- read `/specs` before generating code
- follow the architecture strictly
- avoid modifying SPECs without human approval
