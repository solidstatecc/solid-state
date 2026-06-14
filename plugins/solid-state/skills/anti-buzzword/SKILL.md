---
name: anti-buzzword
description: Flag and rewrite corporate buzzwords, hedge phrases, and throat-clearing. Use when the user wants to "kill the corp speak", "remove fluff", "tighten this", "make this less AI-sounding", or pastes content with classic offenders.
---

# Anti-Buzzword

Find every banned word, throat-clearing phrase, and hedge. Replace with something a builder would actually say.

## The banned list

### Corporate buzzwords (always flag)

synergy, leverage (verb), unlock, robust, holistic, ecosystem, journey, mission, empower, seamless, game-changer, paradigm, disrupt, ideate, granular, low-hanging fruit, circle back, deep dive, move the needle, bandwidth, take it offline, end of the day, scalable solution, stakeholder, value-add, world-class, best-in-class, mission-critical, thought leader, hyperscale, north star, table stakes.

### Hedge phrases (almost always flag)

"I think maybe", "perhaps", "it could be argued", "generally speaking", "in some cases", "to a certain extent", "more or less", "kind of", "sort of", "basically", "essentially", "in many ways", "potentially", "arguably".

### Throat-clearing (always cut)

"In today's fast-paced...", "As we navigate...", "It's important to note that...", "It goes without saying...", "Needless to say...", "At the end of the day...", "When all is said and done...", "First and foremost...".

### Recap phrases (always cut)

"In summary", "To wrap up", "Hopefully this helps", "I hope this gives you", "All in all", "In conclusion", "To recap".

## Process

1. Scan the draft. Mark every match.
2. For each match, propose a replacement. Two options:
   - **Cut** — the sentence works without it.
   - **Replace** — swap with concrete, builder-grade language.
3. Show the diff inline.

## Output template

```
FOUND: 7 issues

1. "leverage our ecosystem"
   → "use the network"
   (banned: leverage, ecosystem)

2. "It's important to note that conversion is up"
   → "Conversion is up."
   (cut: throat-clearing)

3. "We're on a journey to empower builders"
   → "We make tools for builders."
   (banned: journey, empower)

...

CLEAN VERSION
[full rewritten draft]
```

## Rules

- Never replace a buzzword with another buzzword.
- "Leverage" as a noun (Naval-style) is fine. As a verb, kill it.
- If the whole sentence collapses without the buzzword, the sentence was hollow. Cut it entirely.
- One pass. Don't ask for permission.
