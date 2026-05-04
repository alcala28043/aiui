```mermaid
flowchart TD

    %% SPEC CREATION
    A[📝 Create SPEC\n/specs/*.openspec.json]:::spec --> B[🔍 Review SPEC\nConsistency + Dependencies]:::spec

    %% SHARED TYPES
    B --> C[⚙️ Generate Shared Types\n/shared (TS + Rust)]:::shared

    %% FEATURE BRANCH
    C --> D[🌱 Create Feature Branch\nfeature/<name>]:::branch

    %% AI AGENTS
    D --> E[🤖 AI Agents Read SPEC\nCline / Cursor / Windsurf / OpenCode]:::agents
    E --> F[🧩 Generate Code\nFrontend / Backend / Tauri]:::code

    %% LOCAL DEVELOPMENT
    F --> G[🧪 Local Testing\nValidation + Lint + Build]:::local

    %% PULL REQUEST
    G --> H[📤 Open Pull Request → dev]:::pr
    H --> I[👀 Human Review\nSPEC Compliance + Security]:::review

    %% MERGE TO DEV
    I --> J[🔀 Merge into dev]:::merge

    %% RELEASE CANDIDATE
    J --> K[📦 Promote to release\nStaging Build]:::release

    %% FINAL PRODUCTION
    K --> L[🚀 Merge into main\nProduction Release]:::main

    %% STYLES
    classDef spec fill:#1e1e1e,stroke:#555,color:#fff
    classDef shared fill:#2b2b2b,stroke:#666,color:#fff
    classDef branch fill:#333,stroke:#777,color:#fff
    classDef agents fill:#444,stroke:#888,color:#fff
    classDef code fill:#333,stroke:#777,color:#fff
    classDef local fill:#333,stroke:#777,color:#fff
    classDef pr fill:#333,stroke:#777,color:#fff
    classDef review fill:#333,stroke:#777,color:#fff
    classDef merge fill:#333,stroke:#777,color:#fff
    classDef release fill:#333,stroke:#777,color:#fff
    classDef main fill:#333,stroke:#777,color:#fff
```

---

# 🧠 **What this diagram expresses**

### ✔️ SPECs are the origin of everything  
The entire system flows from:

- architecture  
- types  
- validations  
- events  
- rules  

### ✔️ Shared types are generated automatically  
And used by:

- Angular  
- Node backend  
- Tauri Rust  

### ✔️ AI agents work ONLY after reading the SPEC  
They:

- generate code  
- follow rules  
- respect architecture  
- never invent APIs  

### ✔️ Development happens in feature branches  
Never directly in:

- dev  
- release  
- main  

### ✔️ PR → dev → release → main  
The full promotion pipeline is represented visually.

### ✔️ Human review is mandatory  
Even with AI agents, humans approve architecture‑level changes.



