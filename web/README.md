# 🌐 aiui — Public Website

This directory contains the **official aiui website**, including:

- Landing page  
- Documentation  
- Blog / Changelog  
- Roadmap  
- SEO  

The website is **independent** from the desktop application.

---

## 🧱 Recommended Technologies

### 🥇 Astro (recommended)
- Fast  
- Markdown + MDX  
- Perfect for docs + landing  
- Great SEO  

### 🥈 Docusaurus
- Strong documentation system  
- Built‑in blog  
- Versioning  

### 🥉 VitePress
- Minimal  
- Markdown‑first  
- Very fast  

---

## 📂 Suggested Structure

```
web/
├─ src/          → Landing
├─ docs/         → Documentation
├─ blog/         → Blog / Changelog
├─ public/       → Static assets
└─ README.md
```

---

## 🚀 Development (Astro example)

```
cd web
npm install
npm run dev
```

---

## 📦 Deployment

Recommended options:

- GitHub Pages  
- Vercel  
- Netlify  

---

## 🧠 Rules

- The website **does not use SPECs**.  
- The website is **not part of the runtime**.  
- It is purely **marketing + documentation**.  
- Do not mix app code with web code.  

---

## 📜 License

MIT License.
