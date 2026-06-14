# Push solid-state → public repo + confirm the marketplace read

## Step 4 FIRST (local, no push needed) — proves the manifest read in ~1 min
Open Grok in any folder, then in the TUI:
```
/plugins        →  Marketplace tab  →  Add source  →  paste the local path:
/Users/ThorEngelstad/Library/CloudStorage/Dropbox-CalibreStudio/Thor Elias Engelstad/__Visionaire/_Visionaire Labs/__Solid State/GITHUB-NEW/solid-state
```
Then quit and run:
```
grok inspect
```
EXPECT: `Marketplaces (1)` with `solid-state` → `solid-state` plugin (5 skills). That closes the second half of the smoke test. Paste me the result.

---

## Then PUSH for real distribution

```
cd "/Users/ThorEngelstad/Library/CloudStorage/Dropbox-CalibreStudio/Thor Elias Engelstad/__Visionaire/_Visionaire Labs/__Solid State/GITHUB-NEW/solid-state"

# optional cleanup: drop the legacy root manifest (canonical one lives in .claude-plugin/)
rm -f plugin.json

git init -b main
git add -A
git commit -m "Solid State: plugin + marketplace manifest"

# creates the public repo and pushes in one step (needs gh auth — see note)
gh repo create solidstatecc/solid-state --public --source=. --remote=origin --push
```

Notes:
- Repo name `solidstatecc/solid-state` is a choice — change it if you'd rather use `skills-marketplace`.
- If `gh` isn't logged in: run `gh auth login` first (this is the open SOL-22).
- No `gh`? Create the empty repo on github.com, then:
  ```
  git remote add origin git@github.com:solidstatecc/solid-state.git
  git push -u origin main
  ```

After push, the public marketplace source for anyone (and your "add in one line" claim) is:
```
https://github.com/solidstatecc/solid-state
```
