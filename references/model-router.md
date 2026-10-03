# Model Router, Free Backends for the Coding Agent

The standing lesson: a router is not a model. OmniRoute silently dropped to
its weakest always-free tier and the lets-scroll build faked its visuals with
CSS. The fix is never a better prompt, it is pinning a real model and
verifying it answers. Hardware is never the blocker: an i3 with 16GB and no
GPU runs the full pipeline, because inference happens on the provider's
servers.

## The ranking (as of late September 2026)

1. Claude Sonnet via Google Antigravity, free public preview. Proven on this
   exact pipeline. Primary environment for flagship builds: own site,
   Tier 2 chains, first pass on a new vertical.
2. zai-org/GLM-5.3-Flash. The best free OpenCode backend. Strong agentic
   coding, long context, free through OpenCode Zen and through Dahl
   Inference (first 100M tokens free, no card, OpenAI-compatible endpoint).
   Z.ai also runs a free Anthropic-compatible endpoint that drops into
   OpenCode as a key.
3. deepseek-ai/DeepSeek-V4-Flash. Close third, same free routes. Slightly
   better at long reasoning passes (design package drafting, copy passes),
   slightly weaker at multi-file agent loops than GLM.
4. MiniMaxAI/MiniMax-M2.7. Capable, keep it for second passes: long-context
   review, copy critique, plan checking. Not the daily driver.
5. Kimi-K2.6 on Dahl's free 100M pool. Reading-heavy tasks. The kimi.com
   web app is session-based and cannot be wired into OpenCode.
6. GonkaRouter, one-time $20 free credit. Anthropic and OpenAI compatible,
   from $0.0024 per 1M tokens. Overflow when free pools run dry mid-month.

Skip for coding: Jev (TypeSafe). It is a System One model: it returns typed
probabilistic decisions instead of generated text, it is explicitly not a
replacement for a text-generating coding model, and it is waitlisted early
access. Track it for product automation later (fast classification and
routing inside the retainer tools), not for building sites.

## Wiring rules

- One model per build pass. Switching mid-build changes the character of the
  code the way switching video models mid-chain changes the footage.
- Strongest model for the design package and the first build. Flash tiers
  for the edit and polish loops.
- Pin the model ID in the config. After any swap, run a one-line verification
  prompt and read the response's reported model, because a router under
  pressure silently reroutes.
- When a free pool runs out mid-build, finish on the next backend in the
  list rather than letting the router choose.

## OpenDesign (github.com/nexu-io/open-design)

Yes, it plugs in. Local-first, open-source desktop app that turns the coding
agent into the design engine: it previews the files the agent writes and
exports real artifacts, and it lists OpenCode among its supported CLIs via
BYOK. It reads a DESIGN.md from the project.

How to use it without breaking the skill's rules: the Master Brief IS the
DESIGN.md. Paste the approved brief as the project's DESIGN.md, point
OpenCode at it, keep all design decisions in the brief, and let OpenDesign
handle preview and export. It is a preview and delivery layer, not a
decision maker. It never overrides the palette, the type pairing, or the
tier choice.

## Cost honesty for asset generation

Free models cover the code. They do not cover image and video generation.
For that: paid generators (Higgsfield credits, Monid per-clip USD) or the
manual path (the skill writes every prompt plus conditioning frames, the
renders happen in tools of choice). Tier 0 builds need neither: a cinematic
poster hero plus SVG and CSS motion costs nothing and still clears the
quality floor.