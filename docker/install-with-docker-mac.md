# 🚀 Instalación de n8n Self-Hosted en macOS con Docker Compose

Este instructivo explica cómo levantar una instancia local de **n8n** usando **Docker** y **Docker Compose** en macOS.  
Es la misma instalación utilizada en clase, ideal para prácticas y automatizaciones locales.

## 📦 Requisitos

- Docker Desktop → https://www.docker.com/products/docker-desktop/
- Git (opcional)

Verificá la instalación:

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

En lugar de incluir el archivo completo en el README, lo dejamos separado para una mejor organización del proyecto.

Podés ver o descargar el archivo desde este enlace:

👉 **[`docker-compose.yml`](docker-compose.yml)**

Este archivo define el servicio de n8n, los puertos expuestos, las variables de entorno básicas y el volumen para persistir los datos en `./n8n_data/`.


## ▶️ Levantar n8n

```
docker compose up -d
```

Ver logs:

```
docker compose logs -f
```

## 🌐 Acceder

http://localhost:5678

## 🛑 Detener

```
docker compose stop
docker compose down
docker compose down -v   # elimina datos
```

## 🔄 Actualizar

```
docker compose pull
docker compose up -d
```

## 🌍 URLs públicas (ngrok)

```
ngrok http 5678
```

## 🧪 Prueba rápida

1. Crear workflow → Webhook.
2. Responder.
3. Probar con Postman / ReqBin.

## 🛠 Problemas comunes

| Problema | Causa | Solución |
|---------|--------|-----------|
| Puerto 5678 ocupado | Otro proceso usando el puerto | Cambiar a 5679:5678 |
| No persiste | Falta volumen | Revisar carpeta n8n_data |
| Permisos | macOS bloquea escritura | chmod -R 755 n8n_data |
| HTTPS | n8n local no genera | usar ngrok |

