```mermaid
flowchart TD

    %% PROMPTS
    P1[📘 specs_prompt.md\n"How SPECs must be created"]:::prompt
    P2[📘 agents_prompt.md\n"How agents must behave"]:::prompt
    P3[📘 code_from_specs_prompt.md\n"How to generate code from SPECs"]:::prompt

    %% AGENTS
    A1[🤖 Cline\nVS Code Agent]:::agent
    A2[🤖 Cursor\nAI IDE]:::agent
    A3[🤖 Windsurf\nAI Flow IDE]:::agent
    A4[🤖 OpenCode\nLocal AI Dev Agent]:::agent

    %% SPECs
    S[📘 SPECs\nOpenSpec Modules\nSingle Source of Truth]:::spec

    %% SHARED TYPES
    ST[📁 /shared\nGenerated Types\nTS + Rust]:::shared

    %% CODE TARGETS
    FE[🖥️ Frontend\nAngular 21]:::frontend
    BE[🛠️ Backend\nNode + TypeScript]:::backend
    TA[🦀 Tauri\nRust Commands]:::tauri

    %% BRANCHES
    BR[🌱 feature/<name>\nAllowed Branch]:::branch
    PR[📤 Pull Request → dev]:::pr

    %% PROMPT FLOW
    P1 --> S
    P2 --> A1
    P2 --> A2
    P2 --> A3
    P2 --> A4
    P3 --> A1
    P3 --> A2
    P3 --> A3
    P3 --> A4

    %% AGENTS READ SPECs
    A1 --> S
    A2 --> S
    A3 --> S
    A4 --> S

    %% AGENTS GENERATE CODE
    S --> ST
    ST --> FE
    ST --> BE
    ST --> TA

    A1 --> FE
    A1 --> BE
    A1 --> TA

    A2 --> FE
    A2 --> BE
    A2 --> TA

    A3 --> FE
    A3 --> BE
    A3 --> TA

    A4 --> FE
    A4 --> BE
    A4 --> TA

    %% BRANCHING
    A1 --> BR
    A2 --> BR
    A3 --> BR
    A4 --> BR

    BR --> PR

    %% STYLES
    classDef prompt fill:#1e1e1e,stroke:#555,color:#fff
    classDef agent fill:#2b2b2b,stroke:#666,color:#fff
    classDef spec fill:#333,stroke:#777,color:#fff
    classDef shared fill:#444,stroke:#888,color:#fff
    classDef frontend fill:#333,stroke:#777,color:#fff
    classDef backend fill:#333,stroke:#777,color:#fff
    classDef tauri fill:#333,stroke:#777,color:#fff
    classDef branch fill:#333,stroke:#777,color:#fff
    classDef pr fill:#333,stroke:#777,color:#fff
```

---

# 🧠 **What this diagram explains**

### ✔️ 1. Prompts govern everything  
- `specs_prompt.md` → how SPECs are created  
- `agents_prompt.md` → how agents must behave  
- `code_from_specs_prompt.md` → how agents generate code  

### ✔️ 2. All agents read SPECs  
Cline, Cursor, Windsurf y OpenCode **siempre** leen `/specs` antes de generar código.

### ✔️ 3. Shared types are generated from SPECs  
And used by:

- Angular  
- Node backend  
- Tauri Rust  

### ✔️ 4. Agents generate code ONLY in feature branches  
Never in:

- dev  
- release  
- main  

### ✔️ 5. All work ends in a PR → dev  
Human review is mandatory.



