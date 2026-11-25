# Aider + Plugsky

```bash
export OPENAI_API_BASE=https://api.plugsky.com/v1
export OPENAI_API_KEY=$PLUGSKY_API_KEY
aider --model openai/plugsky-pro
```

Or `.aider.conf.yml`:

```yaml
openai-api-base: https://api.plugsky.com/v1
model: openai/plugsky-pro
```

Aider expects the `openai/` model prefix for an OpenAI-compatible endpoint. Use `openai/plugsky-coder` for coding-heavy sessions.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
