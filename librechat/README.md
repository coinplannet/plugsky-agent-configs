# LibreChat + Plugsky

1. Copy `librechat.yaml` to your LibreChat root (or merge the `endpoints.custom` block into your existing file).
2. Set the key in the LibreChat environment:
   ```bash
   PLUGSKY_API_KEY=sk-live-...
   ```
3. Restart LibreChat.
4. In the model picker, choose **Plugsky**, then `plugsky-pro`, `plugsky-max` or `plugsky-lite`.

The base URL includes `/v1`. `fetch: true` pulls the live model list from `https://api.plugsky.com/v1/models`; if discovery is blocked, the three default IDs still work.

Free plan: 100 requests/day, 50K tokens/day, no card. For sustained use, Hobby at $8/month gives 1,000 requests/day, 2M tokens/day and 4 concurrent requests.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
