# 🪟 Instalación de n8n Self-Hosted en Windows con Docker Desktop

Este instructivo explica cómo levantar **n8n self-hosted en Windows** usando **Docker Desktop** y **Docker Compose**.  
Funciona tanto en Windows 10 como en Windows 11 (Home o Pro).

## 📦 Requisitos

### 1️⃣ Docker Desktop para Windows
https://www.docker.com/products/docker-desktop/

> En Windows Home, Docker Desktop usa WSL2. Si no está activado, te lo pedirá.

### 2️⃣ Git (opcional)
https://git-scm.com/download/win

Verificar instalación:

```
docker --version
docker compose version
```

## 📁 Crear el proyecto

```
mkdir n8n-selfhosted
cd n8n-selfhosted
```

## 🧱 Archivo `docker-compose.yml`

El archivo está separado en el repo:

docker-compose.yml

## ▶️ Levantar n8n

```
docker compose up -d
```

Logs:

```
docker compose logs -f
```

## 🌐 Acceder

http://localhost:5678

## 🛑 Detener

```
docker compose stop
docker compose down
docker compose down -v
```

## 🔄 Actualizar

```
docker compose pull
docker compose up -d
```

## 🌍 ngrok

```
ngrok http 5678
```

## 🧪 Prueba rápida

1. Workflow nuevo  
2. Webhook  
3. Respond to Webhook  
4. Probar con Postman  

## 🛠 Problemas comunes

| Problema | Causa | Solución |
|----------|--------|-----------|
| Docker no inicia | WSL2 no activado | `wsl --install` |
| No persiste datos | Volumen bloqueado | borrar `n8n_data` |
| Puerto 5678 ocupado | conflicto | cambiar a 5679 |
| Permisos | OneDrive bloquea | mover el proyecto |

