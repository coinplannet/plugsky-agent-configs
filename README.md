# Plugsky agent configs

Ready-to-paste configuration for using [Plugsky](https://plugsky.com) as an OpenAI-compatible provider in agent frameworks and coding tools.

**Get a key:** https://plugsky.com/ (Free plan, no card) · **Docs:** https://plugsky.com/docs · **MCP:** https://plugsky.com/mcp

> **Free tier reality check:** the free plan is for evaluation — 100 requests/day, 50K tokens/day, 1 concurrent request, 32K input / 2K output, Micro/Lite models. Agent loops burn through that quickly. For sustained agent use, Hobby at $8/month gives 1,000 requests/day, 2M tokens/day, 4 concurrent, 120 RPM and 64K input / 8K output.

## Configs

| Tool | File | Notes |
|---|---|---|
| OpenClaw | [`openclaw/openclaw.json5`](openclaw/openclaw.json5) | `models.providers` escape hatch; declares image input for `plugsky-lite` |
| Hermes Agent | [`hermes/config.yaml`](hermes/config.yaml) | `provider: custom`, `key_env: PLUGSKY_API_KEY` |
| OpenCode | [`opencode/opencode.json`](opencode/opencode.json) | Uses `@ai-sdk/openai-compatible` |
| Codex CLI | [`codex/config.toml`](codex/config.toml) | Responses wire API; must be user-level config |
| LibreChat | [`librechat/librechat.yaml`](librechat/librechat.yaml) | Custom endpoint; `fetch: true` pulls the live model list |
| AnythingLLM | [`anythingllm/README.md`](anythingllm/README.md) | Generic OpenAI provider in Settings → LLM Preference |
| LobeChat | [`lobe-chat/README.md`](lobe-chat/README.md) | OpenAI proxy URL + env |
| NextChat | [`nextchat/README.md`](nextchat/README.md) | Endpoint is host only; do not add `/v1` |
| Jan | [`jan/README.md`](jan/README.md) | UI or `jan config set --base-url` |
| Chatbox | [`chatbox/README.md`](chatbox/README.md) | API Host + `/v1/chat/completions` path |
| Cherry Studio | [`cherry-studio/README.md`](cherry-studio/README.md) | Add Provider → API Host |
| SiYuan | [`siyuan/README.md`](siyuan/README.md) | Custom preset; one-line provider PR |
| Obsidian Copilot | [`obsidian-copilot/README.md`](obsidian-copilot/README.md) | BYOK → Add custom provider |
| Big-AGI | [`big-agi/README.md`](big-agi/README.md) | OpenAI vendor API Host |
| Page Assist | [`page-assist/README.md`](page-assist/README.md) | OpenAI Compatible API → Custom |
| Continue | [`continue/config.yaml`](continue/config.yaml) | Coder + embed roles; `${{ secrets.PLUGSKY_API_KEY }}` |
| Cline | [`cline/README.md`](cline/README.md) | UI steps for the built-in OpenAI Compatible provider |
| Open WebUI | [`openwebui/README.md`](openwebui/README.md) | One env var or Admin → Connections |

## Rules

- Never commit a real key. Every config reads `PLUGSKY_API_KEY` from the environment.
- `plugsky-micro` is text-only; `plugsky-lite` also accepts images.
- The API base is `https://api.plugsky.com/v1`. The MCP endpoint is `https://plugsky.com/mcp` with `Authorization: Bearer $PLUGSKY_API_KEY`.

## Links

- Pricing and limits: https://plugsky.com/pricing
- Free tier details: https://plugsky.com/free-llm-api
- MCP setup: https://plugsky.com/features/mcp
- Model catalogue: https://plugsky.com/models
