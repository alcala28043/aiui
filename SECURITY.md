# 🔐 Security Policy — AIUI

AIUI is a modular, multi‑runtime system (Angular, Node, Tauri, Rust) driven by
OpenSpec architecture. Security is a core requirement across all modules.

This document explains how to report vulnerabilities, how security is handled,
and what contributors (human or AI) must follow to keep the project safe.

---

# 1. Supported Versions

Only the following branches receive security updates:

- `main` — production, stable
- `release` — pre‑production
- `dev` — active development

Feature branches (`feature/*`) are not supported for security patches.

---

# 2. Reporting a Vulnerability

If you discover a security issue, **do NOT open a public GitHub issue**.

Instead, report it privately via:

📧 **security@aiui.dev** (placeholder — replace with your real email)  
or  
🔒 GitHub Security Advisories (recommended)

Please include:

- Description of the vulnerability  
- Steps to reproduce  
- Impact assessment  
- Affected modules (frontend, backend, tauri, shared, specs)  
- Suggested mitigation (optional)

We will respond within **72 hours**.

---

# 3. Security Principles

AIUI follows these core principles:

### ✔️ 3.1 SPEC‑Driven Security
All modules must follow the security rules defined in:

- `07-security.openspec.json`
- Any module‑specific security constraints

No code may bypass or contradict SPEC security rules.

### ✔️ 3.2 Least Privilege
- Backend services must expose only required endpoints  
- Tauri commands must be explicitly whitelisted  
- No wildcard permissions  
- No direct filesystem access unless defined in SPECs  

### ✔️ 3.3 Zero Trust Between Modules
- Frontend never trusts backend responses blindly  
- Backend never trusts frontend input  
- Tauri never trusts external processes  
- All data must be validated at every boundary  

### ✔️ 3.4 No Secrets in the Repo
Forbidden:
- API keys  
- Tokens  
- Passwords  
- Certificates  
- Local environment configs  

Use `.env.local` (ignored by Git).

### ✔️ 3.5 Secure Defaults
- HTTPS everywhere  
- CSP headers in frontend  
- Sanitized user input  
- Escaped output  
- No eval, Function(), or dynamic code execution  

---

# 4. AI Agent Security Rules

AI agents (Cline, Cursor, Windsurf, OpenCode) MUST follow:

### ✔️ 4.1 Never modify security‑critical files without human approval
Forbidden for AI agents:
- `/specs/07-security.openspec.json`
- Tauri `allowlist` config
- Backend authentication middleware
- Permission systems
- Encryption logic

### ✔️ 4.2 Never introduce:
- eval()  
- dynamic imports from user input  
- unsafe Rust code  
- filesystem access not defined in SPECs  
- network calls not defined in SPECs  

### ✔️ 4.3 AI agents must declare security‑sensitive changes in PRs
PR description must include:

```
Security Impact: <none | low | medium | high>
Reason: <explanation>
SPECs referenced: <list>
```

### ✔️ 4.4 AI agents must not bypass branch protections
Agents must work only in:

```
feature/<name>
```

Never in:
- dev  
- release  
- main  

---

# 5. Secure Development Guidelines

### ✔️ 5.1 Backend (Node + TS)
- Validate all input (Zod recommended)
- Use parameterized queries
- Avoid exposing internal errors
- Use strict TypeScript mode
- No global mutable state

### ✔️ 5.2 Frontend (Angular)
- Sanitize HTML
- Avoid bypassSecurityTrust… unless SPEC‑approved
- Use Signals/RxJS safely
- No direct DOM manipulation

### ✔️ 5.3 Tauri (Rust)
- Use the Tauri allowlist
- No arbitrary filesystem access
- No shell execution unless SPEC‑approved
- Avoid unsafe Rust
- Validate all command inputs

### ✔️ 5.4 Shared Types
- Must be generated from SPECs
- No manual editing
- No hidden fields or undocumented properties

---

# 6. Dependency Security

- Use `npm audit` and `cargo audit`
- Update dependencies regularly
- Avoid unmaintained libraries
- Avoid libraries with known CVEs
- Lockfile must be committed

---

# 7. Handling Security Fixes

Security fixes follow this flow:

```
feature/security/<issue> → dev → release → main
```

All fixes must include:

- Root cause analysis  
- SPEC impact  
- Regression tests (if applicable)  

---

# 8. Disclosure Policy

We follow **responsible disclosure**:

- We acknowledge the report privately  
- We fix the issue  
- We release a patched version  
- We publish a security advisory  
- We credit the reporter (optional)

---

# 9. Contact

For any security concerns:

📧 info@kpucha.dev  
🔒 GitHub Security Advisories  
