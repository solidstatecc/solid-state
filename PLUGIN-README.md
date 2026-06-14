# Solid State — Skill Pack

A voice-enforcement plugin for Claude Code, Cowork, and any AI tool that supports skills.

## What's in here

- **`/voice`** — Load the Solid State voice file as conversation context.
- **`/ship-it`** — Run the full pipeline: compress → anti-buzzword → voice-check.
- **voice-check** — Score a draft 0–50 against the rules.
- **anti-buzzword** — Flag every buzzword, hedge, and recap. Auto-rewrite.
- **contrast-pair** — Generate Jack-Butcher-style `X. Not Y.` lines.
- **reframe** — Invert a cliché into a Solid State reframe.
- **compress** — Cut any draft to median 9-word sentences.

## Install

```bash
# Claude Code
claude plugin install solid-state

# Or clone and link locally
git clone https://github.com/solid-state/skill-pack
claude plugin link ./skill-pack
```

## Use

```
You: /voice

[paste your draft]

You: run voice-check on this
```

Or one shot:

```
You: /ship-it

[paste your draft]
```

## Pricing

- **Free** — voice-check, contrast-pair, reframe (rate-limited).
- **$9/mo** — unlimited everything, plus the `/ship-it` pipeline command.
- **$99/yr** — same as monthly, two months free.

## Source

Built on `solidstate.md` — a public, MIT-licensed persona file. Get it at [solidstate.cc](https://solidstate.cc).

## License

Plugin source: MIT. Persona file: MIT. Use it. Fork it. Ship.
