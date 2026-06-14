---
description: Run the full Solid State pipeline on a draft — voice check, anti-buzzword, compress. Returns a ship-ready version.
---

Run the full pipeline on the content I just shared:

1. Compress it (target: 40–60% of input length, median 9-word sentences).
2. Run anti-buzzword on the result.
3. Run voice-check on the cleaned version.
4. If voice-check returns 40+, output the final version.
5. If voice-check returns under 40, run compress + anti-buzzword once more, then output.

Return only the final ship-ready version. No commentary unless I ask.
