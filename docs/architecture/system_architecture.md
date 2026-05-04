```mermaid
flowchart TD

    %% CORE SPEC LAYER
    S[📘 SPECs\n(OpenSpec Modules)\nSingle Source of Truth]:::spec

    %% SHARED TYPES
    ST[📁 /shared\nGenerated Types\n(TypeScript + Rust)]:::shared

    %% FRONTEND
    FE[🖥️ Frontend\nAngular 21\nSignals + RxJS\nStandalone Components]:::frontend

    %% BACKEND
    BE[🛠️ Backend\nNode + TypeScript\nModular Services]:::backend

    %% TAURI
    TA[🦀 Tauri App\nRust Commands\nStrict Allowlist]:::tauri

    %% AI AGENTS
    AG[🤖 AI Agents\nCline / Cursor / Windsurf / OpenCode\n(SPEC‑First Code Generation)]:::agents

    %% FLOWS
    S --> ST
    ST --> FE
    ST --> BE
    ST --> TA

    AG --> S
    AG --> ST
    AG --> FE
    AG --> BE
    AG --> TA

    FE --> BE
    BE --> TA
    TA --> FE

    %% STYLES
    classDef spec fill:#1e1e1e,stroke:#555,color:#fff
    classDef shared fill:#2b2b2b,stroke:#666,color:#fff
    classDef frontend fill:#333,stroke:#777,color:#fff
    classDef backend fill:#333,stroke:#777,color:#fff
    classDef tauri fill:#333,stroke:#777,color:#fff
    classDef agents fill:#444,stroke:#888,color:#fff
```

---

# 🧠 **What this diagram expresses**

### ✔️ SPECs are the core of the system  
Everything flows from them:

- types  
- routes  
- events  
- validations  
- architecture  

### ✔️ Shared types are generated from SPECs  
And used by:

- Angular  
- Node backend  
- Tauri Rust commands  

### ✔️ AI agents operate in a SPEC‑first workflow  
They:

- read SPECs  
- generate code  
- never invent APIs  
- follow branching rules  
- maintain consistency  

### ✔️ Runtime architecture is a triangle  
- Frontend ↔ Backend  
- Backend ↔ Tauri  
- Tauri ↔ Frontend  

### ✔️ The diagram shows both:  
- **Build‑time flow** (SPEC → shared → code)  
- **Runtime flow** (FE ↔ BE ↔ Tauri)  




