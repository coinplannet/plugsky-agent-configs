# WordPress AI Engine + Plugsky

AI Engine supports a custom OpenAI-compatible environment.

**AI Engine → Settings → AI Environments → Add Environment → Custom (OpenAI-Compatible):**

- Endpoint: `https://api.plugsky.com/v1`
- API Key: `sk-live-...`
- Models: `plugsky-pro`, `plugsky-lite`, `plugsky-embed`

The endpoint includes `/v1`; AI Engine appends `/chat/completions`, `/embeddings` and `/models`. Models are auto-discovered from `GET /v1/models`.

Free plan: 100 requests/day, 50K tokens/day. For a content site, Starter or Builder is the realistic starting point.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
