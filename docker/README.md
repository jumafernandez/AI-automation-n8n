# 🐳 Run n8n with Docker

This directory contains a **Docker-based setup** to run **n8n locally**, intended to support the AI automation workflows in this repository.

It provides a simple and reproducible way to start n8n using Docker and Docker Compose.

---

## 📦 Contents

- 🐳 `docker-compose.yml`  
  Docker Compose configuration to run n8n locally.

- 📄 `install-with-docker.md`  
  Step-by-step instructions for Linux and macOS.

- 📄 `install-with-docker-win.md`  
  Step-by-step instructions for Windows (Docker Desktop + WSL2).

---

## ▶️ Quick start

If you already have Docker and Docker Compose installed:

```bash
docker-compose up -d
```

Then open your browser at:

```
http://localhost:5678
```

---

## 💾 Persistence

This setup uses **Docker volumes** to persist:
- workflows
- credentials
- execution data

So your data will remain available across container restarts.

---

## 🔐 Security notes

- This setup is intended for **local development and demos**.
- Basic authentication and HTTPS are not enabled by default.
- For production use, additional security configuration is required.

---

## 🧠 Notes

- Environment variables can be configured in `docker-compose.yml`.
- This setup works both with **self-hosted n8n** and imported workflows from this repository.
