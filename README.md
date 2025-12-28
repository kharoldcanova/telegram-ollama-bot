## Telegram Bot con n8n + Ollama

Bot de Telegram usando n8n y Ollama en local.

### Requisitos
- Docker
- Bot de Telegram
- Ollama corriendo en localhost

### Uso
1. Clonar repo
2. Copiar `.env.example` a `.env`
3. Configurar variables
4. `docker compose up -d`
5. Importar workflow en n8n

### Creacion de chatbot
1. Crear chatbot con BotFather de Telegram

### Exponer ngrok
1. Crear una cuenta de grok
2. Configurar el authtoken
3. `ngrok http 5678`
4. Usar el link publico en WEBHOOK_URL de `.env`

### Ollama (si se usa ollama en el host local)
1. Se debe permitir todos los origenes en el servicio de ollama

`sudo nano /etc/systemd/system/ollama.service`

```
Environment="OLLAMA_HOST=0.0.0.0:11434"
Environment="OLLAMA_ORIGINS=*"
```

2. En Base URL se usa `http://ip-del-servidor:11434`
