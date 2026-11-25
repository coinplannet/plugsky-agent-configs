# Goose + Plugsky

Copy `plugsky.json` to `~/.config/goose/custom_providers/plugsky.json` (Windows: `%APPDATA%\Block\goose\config\custom_providers\`).

Export `PLUGSKY_API_KEY`, then run:

```bash
goose session start --provider plugsky
```

Goose's custom-provider `base_url` includes the full `/chat/completions` path.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
