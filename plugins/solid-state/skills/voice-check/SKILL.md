---
name: voice-check
description: Score any draft against the Solid State voice rules. Use when the user pastes content and asks "is this on-brand?", "does this sound like us?", "review this draft", or any voice-quality check. Returns a score plus specific edits.
---

# Voice Check

Score the draft against the Solid State rules and return specific, actionable edits.

## Process

1. Read `references/solidstate.md` if you haven't already this conversation.
2. Read the user's draft.
3. Score across five dimensions (0–10 each):
   - **Compression** — median sentence length, single-sentence paragraphs, no padding
   - **Contrast** — uses contrast pairs / reframes / compressed math
   - **Directness** — leads with the answer, no throat-clearing, no hedging
   - **Cleanliness** — no buzzwords, no clichés, no recaps
   - **Voice fit** — sounds like a builder, not a chatbot
4. Return the score grid first.
5. Then a "rewrites" section: pick the 3–5 weakest sentences and show before/after.

## Output template

```
SCORE
Compression:  X/10
Contrast:     X/10
Directness:   X/10
Cleanliness:  X/10
Voice fit:    X/10
TOTAL:       XX/50

REWRITES
1. Before: "..."
   After:  "..."
   Why:    [one-line reason]

2. Before: "..."
   After:  "..."
   Why:    [one-line reason]

VERDICT
[Ship / Tighten / Rewrite]
```

## Calibration

- 40+ → Ship. Solid State quality.
- 30–39 → Tighten. Apply the rewrites and re-check.
- <30 → Rewrite. The draft is fighting the voice. Start over.

## Rules

- No diplomacy. If a sentence is dead, say so.
- No "great work, just a few suggestions." If it scored 22 it scored 22.
- Verdict line is one word. "Ship." "Tighten." "Rewrite."
- Never end with "Hope this helps!" or any recap.
