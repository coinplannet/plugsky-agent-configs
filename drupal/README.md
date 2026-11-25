# Drupal AI + Plugsky

The Drupal OpenAI provider stores the host in config; the admin form may not expose it.

```bash
drush config:set ai_provider_openai.settings host https://api.plugsky.com/v1
```

Then create/select a Key entity at `/admin/config/ai/providers/openai` with `sk-live-...`, and choose `plugsky-pro` as the model.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
