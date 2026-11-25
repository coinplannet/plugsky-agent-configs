# AnythingLLM + Plugsky

1. Open **Settings → LLM Preference**.
2. Choose **Generic OpenAI** as the provider.
3. Set:
   - **Base URL:** `https://api.plugsky.com/v1`
   - **API Key:** your `sk-live-...` Plugsky key
   - **Chat Model:** `plugsky-pro`
4. Save, then open a workspace and send a test message.

For the embedding model, use `plugsky-embed` if AnythingLLM asks for a separate embedding provider; the base URL and key are the same.

Free plan: 100 requests/day, 50K tokens/day, no card. Hobby at $8/month is the first plan for sustained agent or workspace use.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
