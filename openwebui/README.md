# Open WebUI

## Docker

```bash
docker run -d -p 3000:8080 \
  -e OPENAI_API_BASE_URL=https://api.plugsky.com/v1 \
  -e OPENAI_API_KEY="$PLUGSKY_API_KEY" \
  -v open-webui:/app/backend/data --name open-webui ghcr.io/open-webui/open-webui:main
```

## Existing deployment

Admin Panel → Settings → Connections → OpenAI API → add:

- Base URL: `https://api.plugsky.com/v1`
- API Key: your Plugsky key

Add it as a second connection if you already use another OpenAI-compatible provider.
