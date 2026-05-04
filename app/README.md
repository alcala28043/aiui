# 🖥️ aiui — Desktop Application

This directory contains the full aiui desktop application:

- **Frontend** → Angular 21  
- **Backend** → Node.js + TypeScript  
- **Runtime** → Tauri 2  
- **Shared types** → TypeScript  

The application runs fully **locally**, with no external services required.

---

## 📂 Structure

```
app/
├─ frontend/     → Angular UI
├─ backend/      → Local API (Node.js + TS)
├─ src-tauri/    → Tauri runtime
└─ shared/       → Shared TypeScript types
```

---

## 🚀 Development

### Frontend

```
cd app/frontend
npm start
```

### Backend

```
cd app/backend
npm run dev
```

### Desktop (Tauri)

```
cd app
npm run tauri dev
```

---

## 🧠 Persistence (v0.1)

aiui **does not use a real database** in version 0.1.

- No SQLite  
- No PostgreSQL  
- No MongoDB  

Persistence is:

- in‑memory  
- mock data  
- JSON files (local)  

The **Storage module** defines the future API for real persistence.

---

## 🧱 Architecture Notes

- Frontend, backend, and Tauri must remain decoupled.
- All types must live in `/app/shared`.
- All behavior must follow the OpenSpec definitions.

---

## 📜 License

MIT License.

