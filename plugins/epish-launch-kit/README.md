# EPISH Campaign Kit for Claude

This package gives Claude the EPISH campaign-kit skill and the connector settings to reach your own EPISH account: copy, a hero plus 3–5 images and a 15–60 second film, then a reviewed publish. The assistant writes under your own Claude plan; EPISH credits pay only for optional generated images and film, and only after you approve the exact price.

## Create your connection link

1. Sign in at https://epish.co with your emailed one-time code and create your profile.
2. Open https://epish.co/bring-your-ai, choose the Claude tab and press `Create my Claude link`.
3. Copy the link now. It is shown once: `https://epish.co/api/connect/<token>/mcp`. You can keep up to 5 active links, each listed with its created and last-used times.

Treat the link like a password. Never commit it, paste it into a public place or put it in this package.

## Use it

claude.ai: add a custom connector in Claude's connector settings and paste the whole link.

Claude Code: install the plugin, then paste your token when Claude Code asks for it. The token is the part of the link between `/api/connect/` and `/mcp`; Claude Code keeps it in its secure storage and sends it as `Authorization: Bearer …` to `https://epish.co/api/connect/mcp`.

```
/plugin marketplace add JuicyMagician/epish-ai
/plugin install epish-launch-kit@epish
```

Change the token later with `/plugin configure epish-launch-kit@epish`. Without the plugin, `claude mcp add --transport http epish <your whole link>` connects the tools without the skills.

Then ask Claude for a campaign page for your idea. Once it is live, ask which ads and links bring backers.

## Revoke

On https://epish.co/bring-your-ai, revoke the link. It stops working at once. Create a new one if you still need access, and save its token with `/plugin configure epish-launch-kit@epish`.

## Status

The skill (`skills/epish-launch-kit/SKILL.md`) is a byte-identical copy of `integrations/skills/epish-launch-kit/SKILL.md`; edit the canonical file. Directory submission has not happened: this package is for local or private installation. It stays unlicensed pending the publisher's distribution decision.
