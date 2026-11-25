# WordPress AI (WPAI) + Plugsky

The core WordPress AI client needs the companion **AI Provider for OpenAI Compatible Servers** plugin.

```bash
wp plugin install ai-provider-for-openai-compatible-servers --activate
wp option update connectors_ai_openai_compatible_servers_base_url https://api.plugsky.com/v1
wp option update connectors_ai_openai_compatible_servers_api_key sk-live-...
wp option update connectors_ai_openai_compatible_servers_model_mode manual
wp option update connectors_ai_openai_compatible_servers_models plugsky-pro,plugsky-lite
```

This is a partial path: it depends on the companion provider plugin, not core alone.

Docs: https://plugsky.com/docs · Pricing: https://plugsky.com/pricing
