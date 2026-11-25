# NextChat + Plugsky

NextChat appends `v1/chat/completions` itself, so the endpoint must **not** include `/v1`.

**UI:** Settings → Custom Endpoint → OpenAI Endpoint `https://api.plugsky.com`, API Key `sk-live-...`, then add `plugsky-lite` or `plugsky-pro` as a custom model.

**Env:**
```env
BASE_URL=https://api.plugsky.com
OPENAI_API_KEY=sk-live-...
```

If you use `https://api.plugsky.com/v1` here, NextChat produces `/v1/v1/chat/completions` and the request fails.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
