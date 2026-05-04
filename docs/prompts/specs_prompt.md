I want you to generate SPECs in OpenSpec format for a modular software project. 
Follow these rules strictly:

1. SPEC structure:
   - $schema
   - id
   - version
   - title
   - description
   - status
   - dependencies
   - types (all required interfaces)
   - frontend (Angular 21)
   - backend (Node + TypeScript)
   - tauri (Rust + allowlist)
   - storage (files, DB, cache)
   - events (internal events)
   - errors (error codes)
   - rules (mandatory rules)
   - edge_cases (edge cases)
   - validations (mandatory validations)
   - todos (pending tasks)

2. Level of detail:
   - Ultra‑detailed (Level D)
   - No ambiguity
   - No “optional” fields unless justified
   - Everything must be explicitly defined: types, routes, flows, states, naming, permissions

3. Philosophy:
   - SPECs are the single source of truth
   - Do not invent anything outside the architecture
   - Do not contradict other SPECs
   - Maintain consistency across modules
   - Use clean, professional naming conventions

4. Technologies:
   - Frontend: Angular 21 + Signals + RxJS + Standalone Components
   - Backend: Node + TypeScript (modular)
   - Tauri: Rust + Commands + strict allowlist
   - Storage: JSON, SQLite, or whatever the SPEC defines
   - Shared types: always generated from SPECs

5. AI agent rules:
   - SPECs must include clear instructions for AI agents (Cline, Cursor, Windsurf, OpenCode)
   - Must specify what agents CANNOT modify
   - Must specify how agents should generate code
   - Must specify how agents validate compliance with the SPEC

6. Style:
   - Professional
   - Clean
   - Consistent
   - No redundant text
   - No explanations outside the SPEC

7. Output:
   - Provide the full SPEC in a single JSON block
   - No comments outside the JSON
   - No extra text before or after the SPEC

When I request a SPEC, generate the complete file following these rules.
