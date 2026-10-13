# @core/kit-landing

[![genpm](https://api.genpm.net/v1/badge/@core/kit-landing.svg)](https://genpm.net/p/@core/kit-landing) ![license](https://img.shields.io/badge/license-MIT-blue)

> Landing page kit for Next.js: block-built pages, lead forms, cookie banner and consent-gated pixels with dedup

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/app/(landing)`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/kit-landing
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/kit-landing`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/kit-landing with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Conversion landing pages on top of @core/kit-cms: the `landings` collection (blocks, SEO, minimal layout without
site navigation, conversion goal, thank-you page) served at `/lp/<slug>`, lead forms that store the submission with
its UTM parameters and fire one deduplicated `lead` event (server + browser with the same `eventId`, only with
consent), a cookie banner, consent-gated GA4/Meta/TikTok pixels and a real-deadline countdown block.
A/B tests with @core/experiments: a landing can name an experiment and show `blocksB` to variant `b`.

## At a glance

- **GenPM dependencies** (installed with it): [@core/kit-cms](https://genpm.net/p/@core/kit-cms), [@core/consent](https://genpm.net/p/@core/consent), [@core/pixels](https://genpm.net/p/@core/pixels), [@core/experiments](https://genpm.net/p/@core/experiments)
- **npm dependencies** (proposed, never installed without asking): `next`, `react`, `zod`
- **Environment variables** (added to `.env.example`): `GA4_MEASUREMENT_ID`, `META_PIXEL_ID`, `TIKTOK_PIXEL_ID`, `CONSENT_POLICY_VERSION`, `EXPERIMENTS_SECRET`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/app/(landing)`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
