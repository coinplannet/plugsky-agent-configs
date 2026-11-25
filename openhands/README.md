# OpenHands + Plugsky

In **Settings → LLM → Advanced**, set:

- Custom Model: `openai/plugsky-pro`
- Base URL: `https://api.plugsky.com/v1`
- API Key: your Plugsky key

Or persist the profile with:

```json
{
  "llm": {
    "model": "openai/plugsky-pro",
    "base_url": "https://api.plugsky.com/v1",
    "api_key": "<PLUGSKY_API_KEY>"
  }
}
```

The model must carry the `openai/` prefix. OpenHands validates the endpoint before saving.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
