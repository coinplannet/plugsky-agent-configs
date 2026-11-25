# SiYuan + Plugsky

SiYuan's provider presets are plain objects with a `baseURL`.

**UI:** Settings → AI → Provider → Custom, then base URL `https://api.plugsky.com/v1`, key and model `plugsky-pro`.

**Preset PR** (add to `app/src/config/tabs/ai/aiProviderPresets.ts`):

```ts
{id: "plugsky", name: "Plugsky", baseURL: "https://api.plugsky.com/v1", category: "aggregator", responsesSupport: "supported"},
```

`category: "aggregator"` makes the API key required, which is correct for Plugsky. Add an SVG only if the PR includes one.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
