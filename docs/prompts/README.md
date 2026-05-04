# AIUI Prompt Suite

This directory contains the master prompts used to generate and maintain the
AIUI architecture, SPECs, and codebase.  
These prompts ensure consistency, enforce project rules, and guide both humans
and AI agents (Cline, Cursor, Windsurf, OpenCode) when contributing to the
project.

The prompts in this folder are part of the AIUI governance layer and define how
SPECs, code, and automated contributions must be produced.

---

## 📁 Files Overview

### 1. specs_prompt.md
**Purpose:**  
Defines the master prompt used to generate new OpenSpec modules.

**Used when:**  
- Creating a new SPEC  
- Expanding the architecture  
- Ensuring consistency across modules  

**Guarantees:**  
- Ultra‑detailed SPECs  
- Consistent structure  
- No ambiguity  
- Full alignment with AIUI architecture  
- SPECs become the single source of truth

---

### 2. agents_prompt.md
**Purpose:**  
Defines how AI agents must behave when working inside the AIUI repository.

**Used by:**  
- Cline  
- Cursor  
- Windsurf  
- OpenCode  
- Any automated contributor  

**Enforces:**  
- SPEC‑first development  
- Branching model (feature → dev → release → main)  
- File boundaries (what agents can and cannot modify)  
- Code quality rules  
- Validation and error‑handling rules  
- PR requirements  

This prompt ensures that AI agents never break the architecture or the repo.

---

### 3. code_from_specs_prompt.md
**Purpose:**  
Defines how AI agents must generate production‑ready code from existing SPECs.

**Used when:**  
- Implementing a module  
- Generating frontend, backend, or Tauri code  
- Creating new features based on SPEC definitions  

**Enforces:**  
- Correct file placement  
- Strict adherence to SPECs  
- Use of shared types  
- No invented APIs  
- No placeholder code  
- Full validation and error handling  
- Clean, modular, consistent implementation  

This prompt ensures that code generated from SPECs is correct, complete, and
aligned with the architecture.

---

## 🧠 Why These Prompts Exist

AIUI is a SPEC‑driven system.  
To maintain consistency and prevent architectural drift, all contributions—
human or AI—must follow the same rules.

These prompts:

- enforce consistency  
- prevent accidental architectural changes  
- ensure safe AI‑generated code  
- maintain long‑term project integrity  
- allow multiple agents to collaborate without conflicts  

They are part of the project's **governance layer**.

---

## 🚀 How to Use These Prompts

### When generating a new SPEC:
Use `specs_prompt.md`.

### When an AI agent is working inside the repo:
Load `agents_prompt.md`.

### When generating code from an existing SPEC:
Use `code_from_specs_prompt.md`.

---

## 🔒 Important Notes

- These prompts MUST NOT be modified without a dedicated PR.  
- Changes to these prompts affect the entire development workflow.  
- AI agents must always follow these prompts before generating code or making changes.

---

## 📜 License

These prompts are part of the AIUI documentation and follow the project's main license.
