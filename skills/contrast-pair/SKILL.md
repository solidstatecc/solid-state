---
name: contrast-pair
description: Generate Jack-Butcher-style contrast pairs. Use when the user wants a "tagline", "headline", "one-liner", "hero copy", "ad", or describes a concept and asks for a "contrast pair", "X. Not Y. version", or anything that should compress into a single visual idea.
---

# Contrast Pair

Generate `X. Not Y.` constructions. The gap between X and Y carries the meaning.

## The template

```
[Thing we are]. Not [thing we get mistaken for].
```

Or:

```
[What we do]. Not [what other people do].
```

## Process

1. Read the concept the user describes.
2. Identify the closest, most flattering misconception.
3. Generate 5 candidates. Each one:
   - X is what we want to be.
   - Y is the closest thing we are NOT.
   - X and Y should rhyme, alliterate, or share a syllable count.
   - Total under 12 words.

## Examples

**Brief:** Solid State product positioning.
- Tools, not toys.
- Skills, not summaries.
- Signal, not noise.
- Builders, not browsers.
- Output, not opinion.

**Brief:** A new CRM for solo operators.
- A workspace. Not a workflow.
- For closers. Not categorizers.
- One operator. Not one-size-fits-all.

**Brief:** A productivity course.
- Output, not optimization.
- Compounding, not consuming.
- Discipline, not dopamine.

## Rules

- 5 candidates minimum.
- Rank them. Lead with the strongest.
- One line each. No explanation under each one.
- After the list, one paragraph max on which to use where (hero, social, deck title).
- If the user gives feedback, generate 5 fresh ones — don't tweak the rejected batch.

## Anti-patterns

- Don't pad: "We are tools, not toys." → just `Tools, not toys.`
- Don't soften: "More tools than toys." kills the gap.
- Don't sprawl: 4-word maximum on each side.
