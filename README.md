# 🧠 aiui — The Unified Local AI Interface

**aiui** is a cross‑platform desktop application that unifies your entire local and remote AI ecosystem into a single, modern, extensible interface.

It integrates:

- Local models (Ollama, LM Studio, custom runtimes)
- API models (OpenAI, Anthropic, Groq, etc.)
- Agents
- Workflows
- Tools
- MCP servers
- LSP servers
- IDE integrations
- Plugins
- A future marketplace

Everything is defined through **OpenSpec**, the single source of truth for the entire system.

---

## 🎯 Objective

To provide a unified, powerful, offline‑first desktop interface for managing:

- AI models  
- Agents  
- Workspaces  
- Projects  
- Tools  
- Workflows  
- Plugins  
- Local runtimes  

All with a clean UX, modular architecture, and full extensibility.

---

## 🧱 Repository Architecture

```
aiui/
├─ app/        → Desktop application (Angular + Backend + Tauri)
├─ specs/      → OpenSpec definitions (source of truth)
├─ web/        → Public website (landing + documentation)
└─ README.md
```

---

## 🚀 Development

### Install dependencies

```
npm install
```

### Run the desktop app

```
cd app
npm run tauri dev
```

---

## 📚 Specifications (OpenSpec)

All architecture, modules, types, routes, and behaviors are defined in:

```
/specs
```

Nothing is implemented unless it exists in a SPEC.

---

## 📜 License

MIT License.