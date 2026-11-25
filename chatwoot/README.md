# Chatwoot + Plugsky

Chatwoot Captain appends `/v1` itself, so the endpoint must **not** include it.

**Super Admin → App Config → Captain:**

- OpenAI API Endpoint: `https://api.plugsky.com`
- OpenAI API Key: `sk-live-...`
- OpenAI Model: `plugsky-pro`
- Embedding Model: `plugsky-embed`

Or via env:
```env
CAPTAIN_OPEN_AI_ENDPOINT=https://api.plugsky.com
CAPTAIN_OPEN_AI_API_KEY=sk-live-...
CAPTAIN_OPEN_AI_MODEL=plugsky-pro
CAPTAIN_EMBEDDING_MODEL=plugsky-embed
```

If you set the endpoint to `https://api.plugsky.com/v1`, Chatwoot calls `/v1/v1/...` and fails.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
