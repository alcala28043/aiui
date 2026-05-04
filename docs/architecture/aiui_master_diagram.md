```mermaid
flowchart TD

    %% GOVERNANCE LAYER
    G[🏛️ Governance Layer\n/docs/prompts\nRules for SPECs, Agents, Code]:::gov

    G --> P1[📘 specs_prompt.md\n"How SPECs are created"]:::prompt
    G --> P2[📘 agents_prompt.md\n"How agents must behave"]:::prompt
    G --> P3[📘 code_from_specs_prompt.md\n"How to generate code from SPECs"]:::prompt

    %% SPEC LAYER
    P1 --> S[📘 SPECs\n/specs/*.openspec.json\nSingle Source of Truth]:::spec

    %% SHARED TYPES
    S --> ST[📁 /shared\nGenerated Types\nTS + Rust]:::shared

    %% AGENTS
    P2 --> A1[🤖 Cline]:::agent
    P2 --> A2[🤖 Cursor]:::agent
    P2 --> A3[🤖 Windsurf]:::agent
    P2 --> A4[🤖 OpenCode]:::agent

    P3 --> A1
    P3 --> A2
    P3 --> A3
    P3 --> A4

    %% AGENTS READ SPECs
    A1 --> S
    A2 --> S
    A3 --> S
    A4 --> S

    %% AGENTS USE SHARED TYPES
    A1 --> ST
    A2 --> ST
    A3 --> ST
    A4 --> ST

    %% CODE GENERATION TARGETS
    ST --> FE[🖥️ Frontend\nAngular 21\nSignals + RxJS]:::frontend
    ST --> BE[🛠️ Backend\nNode + TypeScript]:::backend
    ST --> TA[🦀 Tauri\nRust Commands]:::tauri

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

    %% BRANCHING MODEL
    FE --> BR[🌱 feature/<name>\nAllowed Branch]:::branch
    BE --> BR
    TA --> BR

    BR --> PR[📤 Pull Request → dev]:::pr
    PR --> HR[👀 Human Review\nSPEC Compliance + Security]:::review
    HR --> DEV[🔀 Merge → dev]:::merge
    DEV --> REL[📦 Promote → release]:::release
    REL --> MAIN[🚀 Merge → main\nProduction Release]:::main

    %% RUNTIME FLOW
    MAIN --> RUNTIME[⚡ Runtime System]:::runtime

    RUNTIME --> FE_RT[🖥️ Frontend Runtime]:::frontend
    RUNTIME --> BE_RT[🛠️ Backend Runtime]:::backend
    RUNTIME --> TA_RT[🦀 Tauri Runtime]:::tauri

    FE_RT <--> BE_RT
    BE_RT <--> TA_RT
    TA_RT <--> FE_RT

    %% STYLES
    classDef gov fill:#1e1e1e,stroke:#555,color:#fff
    classDef prompt fill:#2b2b2b,stroke:#666,color:#fff
    classDef spec fill:#333,stroke:#777,color:#fff
    classDef shared fill:#444,stroke:#888,color:#fff
    classDef agent fill:#555,stroke:#999,color:#fff
    classDef frontend fill:#333,stroke:#777,color:#fff
    classDef backend fill:#333,stroke:#777,color:#fff
    classDef tauri fill:#333,stroke:#777,color:#fff
    classDef branch fill:#333,stroke:#777,color:#fff
    classDef pr fill:#333,stroke:#777,color:#fff
    classDef review fill:#333,stroke:#777,color:#fff
    classDef merge fill:#333,stroke:#777,color:#fff
    classDef release fill:#333,stroke:#777,color:#fff
    classDef main fill:#333,stroke:#777,color:#fff
    classDef runtime fill:#1e1e1e,stroke:#555,color:#fff
```

---

# 🧠 **What this master diagram represents**

### ✔️ 1. Governance layer  
The prompts define the rules of the entire system.

### ✔️ 2. SPECs as the single source of truth  
Everything flows from SPECs.

### ✔️ 3. Shared types unify the whole stack  
Angular, Node, and Rust all use the same types.

### ✔️ 4. AI agents operate under strict rules  
They read SPECs → generate code → follow branching model.

### ✔️ 5. Branching model is enforced  
Only feature branches → PR → dev → release → main.

### ✔️ 6. Runtime is a triangle  
Frontend ↔ Backend ↔ Tauri.

### ✔️ 7. Build‑time and runtime are clearly separated  
SPECs → build → deploy → runtime.


