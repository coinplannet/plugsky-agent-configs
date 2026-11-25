# Plugsky agent configs

Ready-to-paste configuration for using [Plugsky](https://plugsky.com) as an OpenAI-compatible provider in agent frameworks and coding tools.

**Get a key:** https://plugsky.com/ (Free plan, no card) · **Docs:** https://plugsky.com/docs · **MCP:** https://plugsky.com/mcp

> **Free tier reality check:** the free plan is for evaluation — 100 requests/day, 50K tokens/day, 1 concurrent request, 32K input / 2K output, Micro/Lite models. Agent loops burn through that quickly. For sustained agent use, Hobby at $8/month gives 1,000 requests/day, 2M tokens/day, 4 concurrent, 120 RPM and 64K input / 8K output.

## Configs

### Chat UIs and desktop clients

| Tool | File | Notes |
|---|---|---|
| LibreChat | [`librechat/librechat.yaml`](librechat/librechat.yaml) | Custom endpoint; `fetch: true` pulls the live model list |
| AnythingLLM | [`anythingllm/README.md`](anythingllm/README.md) | Generic OpenAI provider in Settings → LLM Preference |
| LobeChat | [`lobe-chat/README.md`](lobe-chat/README.md) | OpenAI proxy URL + env |
| NextChat | [`nextchat/README.md`](nextchat/README.md) | Endpoint is host only; do not add `/v1` |
| Jan | [`jan/README.md`](jan/README.md) | UI or `jan config set --base-url` |
| Chatbox | [`chatbox/README.md`](chatbox/README.md) | API Host `…/v1` + path `/chat/completions` |
| Cherry Studio | [`cherry-studio/README.md`](cherry-studio/README.md) | Add Provider → API Host |
| Obsidian Copilot | [`obsidian-copilot/README.md`](obsidian-copilot/README.md) | BYOK → Add custom provider |
| Big-AGI | [`big-agi/README.md`](big-agi/README.md) | OpenAI vendor API Host |
| Page Assist | [`page-assist/README.md`](page-assist/README.md) | OpenAI Compatible API → Custom |
| Open WebUI | [`openwebui/README.md`](openwebui/README.md) | One env var or Admin → Connections |

### Coding agents and agent frameworks

| Tool | File | Notes |
|---|---|---|
| OpenClaw | [`openclaw/openclaw.json5`](openclaw/openclaw.json5) | `models.providers` escape hatch; declares image input for `plugsky-lite` |
| Hermes Agent | [`hermes/config.yaml`](hermes/config.yaml) | `provider: custom`, `key_env: PLUGSKY_API_KEY` |
| OpenCode | [`opencode/opencode.json`](opencode/opencode.json) | Uses `@ai-sdk/openai-compatible` |
| Codex CLI | [`codex/config.toml`](codex/config.toml) | Responses wire API; must be user-level config |
| Cline | [`cline/README.md`](cline/README.md) | Built-in OpenAI Compatible provider |
| Aider | [`aider/README.md`](aider/README.md) | `OPENAI_API_BASE` + `openai/plugsky-pro` |
| Goose | [`goose/plugsky.json`](goose/plugsky.json) | Custom provider JSON; full `/chat/completions` base |
| Zed | [`zed/settings.json`](zed/settings.json) | `language_models.openai_compatible` |
| OpenHands | [`openhands/README.md`](openhands/README.md) | `openai/plugsky-pro` + base URL |
| Continue | [`continue/config.yaml`](continue/config.yaml) | Coder + embed roles; `${{ secrets.PLUGSKY_API_KEY }}` |
| Open Interpreter | [`open-interpreter/config.toml`](open-interpreter/config.toml) | TOML custom provider; `wire_api = "chat"` |

### CMS, support, LMS and team chat

| Tool | File | Notes |
|---|---|---|
| Chatwoot | [`chatwoot/README.md`](chatwoot/README.md) | Endpoint **without** `/v1`; Captain appends it |
| WordPress AI Engine | [`wordpress-ai-engine/README.md`](wordpress-ai-engine/README.md) | Custom (OpenAI-Compatible) environment |
| WordPress AI Puffer | [`wordpress-ai-puffer/README.md`](wordpress-ai-puffer/README.md) | Base without `/v1`, version `v1` |
| WordPress AI (WPAI) | [`wordpress-wpai/README.md`](wordpress-wpai/README.md) | Needs the companion provider plugin |
| Drupal AI | [`drupal/README.md`](drupal/README.md) | `ai_provider_openai.settings:host` via Drush |
| Nextcloud Assistant | [`nextcloud/README.md`](nextcloud/README.md) | Service URL includes `/v1` |
| Moodle | [`moodle/README.md`](moodle/README.md) | Full `/v1/chat/completions` endpoint per action |
| Mattermost Agents | [`mattermost/README.md`](mattermost/README.md) | OpenAI Compatible; Responses off |
| Directus | [`directus/README.md`](directus/README.md) | OpenAI-Compatible Provider; may be plan-gated |
| Discourse AI | [`discourse/README.md`](discourse/README.md) | Full `/v1/chat/completions` endpoint |
| Rocket.Chat | [`rocketchat/README.md`](rocketchat/README.md) | AI Center; enterprise/AI licence |
| Zammad | [`zammad/README.md`](zammad/README.md) | Custom (OpenAI Compatible); embedding size 2048 |
| Flarum AI | [`flarum/README.md`](flarum/README.md) | OpenAI-compatible server connection |
| SiYuan | [`siyuan/README.md`](siyuan/README.md) | Custom provider recipe; no built-in preset PR |

## Rules

- Never commit a real key. Every config reads `PLUGSKY_API_KEY` from the environment.
- `plugsky-micro` is text-only; `plugsky-lite` also accepts images.
- The API base is `https://api.plugsky.com/v1`. The MCP endpoint is `https://plugsky.com/mcp` with `Authorization: Bearer $PLUGSKY_API_KEY`.

## Links

- Pricing and limits: https://plugsky.com/pricing
- Free tier details: https://plugsky.com/free-llm-api
- MCP setup: https://plugsky.com/features/mcp
- Model catalogue: https://plugsky.com/models
