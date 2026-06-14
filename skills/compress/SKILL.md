---
name: compress
description: Compress any draft to Solid State sentence-length targets. Use when the user wants something "shorter", "tighter", "cut to half", "compress this", "Karpathy-ify this", or pastes long-form prose that needs to read like a builder wrote it.
---

# Compress

Cut the draft until the median sentence is under 10 words and every remaining sentence pulls weight.

## Targets

- Median sentence: 9 words.
- Max sentence: 18 words. Anything longer must justify itself.
- Single-sentence paragraphs are encouraged.
- Total output: 40–60% of input length.

## Process

1. Read the draft.
2. Pass 1 — kill throat-clearing, recaps, transitions ("Furthermore", "However it's important to note", "In addition to this").
3. Pass 2 — replace nominalizations with verbs ("the implementation of" → "implementing").
4. Pass 3 — split run-on sentences. One idea per sentence.
5. Pass 4 — cut adjectives that don't change the meaning ("very", "quite", "really", "actually").
6. Pass 5 — read the result aloud. Cut anything you'd skim.

## Output

Return the compressed version. No commentary, no diff, no explanation.

If the user wants a diff, they'll ask. Default is: ship the rewrite.

## Length report (optional, only if asked)

```
INPUT:    412 words
OUTPUT:   178 words (-57%)
MEDIAN:   8 words
MAX:      16 words
```

## Rules

- Never expand. Compression only.
- Never add hedging to "soften" the cuts.
- Never preserve a sentence because the user wrote it. Every sentence earns its place or dies.
- If the input is already at target length, say so in one line and stop.
