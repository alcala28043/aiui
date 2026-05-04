# AIUI Documentation

The `/docs` directory contains all high‑level documentation for the AIUI project.
This includes architectural guidelines, governance rules, development workflows,
and the master prompts used by humans and AI agents.

AIUI is a SPEC‑driven system.  
The documentation in this folder defines how SPECs are created, how code is
generated from them, and how contributors (human or AI) must interact with the
project.

---

## 📁 Directory Structure

```
/docs
/prompts        → Master prompts for SPECs, agents, and code generation
/architecture   → (optional) High‑level system diagrams and conceptual docs
/guides         → (optional) Developer guides, onboarding, workflows
```

Only `/prompts` is mandatory; the other folders may be added as the project
grows.

---

## 🧠 Documentation Philosophy

AIUI follows a **SPEC‑first** philosophy:

- SPECs define the architecture  
- Documentation defines the rules for creating and using SPECs  
- Code is generated from SPECs  
- AI agents must follow the documentation and SPECs strictly  

This ensures long‑term consistency, prevents architectural drift, and allows
multiple agents and humans to collaborate safely.

---

## 📚 Key Components

### 1. `/docs/prompts`
Contains the **master prompts** that govern how SPECs and code are generated.

These prompts define:

- How SPECs must be written  
- How AI agents must behave  
- How code must be generated from SPECs  
- What rules cannot be broken  
- How to maintain consistency across the entire project  

This folder is part of the **governance layer** of AIUI.

---

### 2. Architecture Documentation (optional)
If present, this folder contains:

- High‑level diagrams  
- System overviews  
- Module relationships  
- Data flow diagrams  
- Conceptual explanations  

These documents complement SPECs but do not replace them.

---

### 3. Developer Guides (optional)
If present, this folder contains:

- Onboarding guides  
- Workflow explanations  
- Branching model details  
- Contribution rules  
- Coding standards  

These guides help humans understand how to work within the AIUI ecosystem.

---

## 🔒 Governance Rules

- Documentation in `/docs` MUST NOT be modified casually.  
- Any change requires a dedicated PR and human review.  
- Changes to prompts affect the entire development workflow.  
- Documentation must remain consistent with SPECs and the branching model.  

---

## 🚀 How Documentation Is Used

### When creating a new SPEC:
Use the master prompt in `/docs/prompts/specs_prompt.md`.

### When an AI agent contributes code:
It must follow `/docs/prompts/agents_prompt.md`.

### When generating code from a SPEC:
Use `/docs/prompts/code_from_specs_prompt.md`.

### When onboarding a new contributor:
Point them to `/docs/` as the starting point.

---

## 📜 License

All documentation in this folder follows the project's main license.
