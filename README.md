# EPISH for Claude and ChatGPT

Turn a product idea into a crowdfunding campaign on [epish.co](https://epish.co) from the assistant you already use: story, goal, rewards, FAQs, images and film, then a page you review before anything is published. After launch, ask which ads and links bring backers.

## 1. Get your connection link

Sign in at [epish.co/bring-your-ai](https://epish.co/bring-your-ai), open the Claude tab and press **Create my Claude link**. The link is shown once. Treat it like a password.

## 2. Connect your assistant

**Claude Code** (plugin: the EPISH tools plus two campaign skills)

```
/plugin marketplace add JuicyMagician/epish-ai
/plugin install epish-launch-kit@epish
```

Claude Code asks for your token: the part of your link between `/api/connect/` and `/mcp`. Change it later with `/plugin configure epish-launch-kit@epish`.

**Claude (web, desktop, mobile):** Settings → Connectors → Add custom connector, and paste the whole link.

**ChatGPT:** Settings → Apps → Create app (developer mode), paste the whole link as the MCP server URL, no authentication.

**Any other MCP client:** add `https://epish.co/api/connect/mcp` as a streamable HTTP server with the header `Authorization: Bearer <token>`, or use the whole link as the server URL.

## 3. Start

Say: *"Help me turn my idea into an EPISH campaign."*

Everything is saved as a private draft. Nothing is published, paid for or posted without you approving it in the conversation. Optional AI images and film use EPISH credits and are always quoted first.

## Revoke

Revoke the link at [epish.co/bring-your-ai](https://epish.co/bring-your-ai). It stops working at once.

## Privacy

[epish.co/privacy](https://epish.co/privacy). EPISH is run by X Projects ApS, Denmark.
