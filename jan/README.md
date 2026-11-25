# Jan + Plugsky

**UI:** Settings → Providers → Add Provider → OpenAI, then base URL `https://api.plugsky.com/v1`, key and model IDs `plugsky-lite`, `plugsky-pro`.

**CLI:**
```bash
jan config set \
  --provider openai \
  --api-key "$PLUGSKY_API_KEY" \
  --base-url https://api.plugsky.com/v1 \
  --model plugsky-lite \
  --model plugsky-pro \
  --api-type openai
```

Jan requires `https://` for a remote base URL.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
