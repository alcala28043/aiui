# 📚 aiui — OpenSpec Definitions

This directory contains **all official OpenSpec files** that define the entire aiui architecture.

OpenSpec is the **single source of truth** for:

- Modules  
- Types  
- Routes  
- Services  
- Permissions  
- UX rules  
- Behaviors  
- Dependencies  

Nothing is implemented unless it exists in a SPEC.

---

## 📂 Structure

```
specs/
├─ 00-core-architecture.openspec.json
├─ 01-frontend-foundation.openspec.json
├─ 02-backend-foundation.openspec.json
├─ 03-desktop-runtime.openspec.json
├─ 04-shared-types.openspec.json
├─ 05-ux-design-system.openspec.json
├─ 06-settings-module.openspec.json
├─ 07-security-permissions.openspec.json
├─ 08-storage-module.openspec.json
├─ 09-system-diagnostics.openspec.json
├─ 10-notifications-module.openspec.json
├─ 11-updates-module.openspec.json
├─ 12-telemetry-module.openspec.json
├─ 13-profiles-module.openspec.json
├─ 14-workspaces-module.openspec.json
├─ 15-projects-module.openspec.json
├─ 16-models-module.openspec.json
├─ 17-mcps-module.openspec.json
├─ 18-agents-module.openspec.json
├─ 19-lsps-module.openspec.json
├─ 20-skills-module.openspec.json
├─ 21-workflows-module.openspec.json
├─ 22-tools-module.openspec.json
├─ 22b-ides-module.openspec.json
├─ 23-plugins-system.openspec.json
├─ 24-marketplace-ecosystem.openspec.json
├─ 25-app-distribution-and-packaging.openspec.json
├─ README.md
└─ INDEX.md
```

---

## 🧠 Persistence (v0.1)

The **Storage module** defines the architecture for persistence,  
but **no real database is used in v0.1**.

Implementation is:

- mock  
- in‑memory  
- JSON files  

Real persistence will be added in future versions.

---

## 🧭 Reading Order

1. Core (00–04)  
2. UX (05)  
3. Infrastructure (06–15)  
4. Functional modules (16–22b)  
5. Ecosystem (23–24)  
6. Distribution (25)  

---

## 📜 License

MIT License.
