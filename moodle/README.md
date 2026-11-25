# Moodle + Plugsky

Moodle's OpenAI provider asks for a full endpoint per action.

**Site administration → AI → Providers → OpenAI API provider → action (Generate / Summarise / Explain):**

- API endpoint: `https://api.plugsky.com/v1/chat/completions`
- API key: `sk-live-...`
- Model: `plugsky-pro`

Use the full `/v1/chat/completions` path, not a base URL. Repeat for each action you enable.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
