# Nextcloud Assistant + Plugsky

Install the **OpenAI integration** app for Nextcloud Assistant.

**Settings → Administration → Artificial intelligence → Connected services → Add service:**

- Service URL: `https://api.plugsky.com/v1`
- Service name: `Plugsky`
- API key: `sk-live-...`

Then choose `plugsky-pro` for text and `plugsky-embed` for embeddings. Models are fetched from `GET /v1/models`.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
