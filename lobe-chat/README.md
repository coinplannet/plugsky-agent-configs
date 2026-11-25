# LobeChat + Plugsky

LobeChat's OpenAI provider accepts a proxy/compatible URL.

**UI:** Settings → AI Providers → OpenAI → set the API proxy URL to `https://api.plugsky.com/v1`, paste your Plugsky key, then enable `plugsky-lite` and `plugsky-pro`.

**Deployment env:**
```env
OPENAI_API_KEY=sk-live-...
OPENAI_PROXY_URL=https://api.plugsky.com/v1
OPENAI_MODEL_LIST=+plugsky-lite,+plugsky-pro,+plugsky-reasoning
```

Click **Check** after saving. The base URL includes `/v1`.

Free plan: 100 requests/day, 50K tokens/day, no card. For a team, use Hobby $8 or Starter $20.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
