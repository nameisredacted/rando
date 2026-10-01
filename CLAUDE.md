# Rando

Single destination for quick, truly random picks. Live at https://nameisredacted.github.io/rando (GitHub Pages, `main` / root). Single file: `index.html`. Mirror copy kept in `~/Desktop/Invisible Hand/WIP/Rando/index.html` on the user's Mac.

## v1 — numbers (complete, 2026-09-30)
- Range always starts at 1 (inclusive); top number starts blank.
- Input: type the top number and press Return/Enter (iOS "Go"), or tap the mic and speak ("fifty", "one to twenty", "again"). Tapping the big result re-rolls.
- Randomness: `crypto.getRandomValues` with rejection sampling (unbiased), up to 2^53.
- Voice: Web Speech API; needs https hosting (artifact iframes block the mic). Result is read aloud when the roll came from voice.

## Design rules (user-set — keep)
- Black background, system font (SF on Apple), thin weights. No boxes, no borders, no Roll button.
- The bottom line reads `1 – [top]`; the 1 and the dash are the same white as everything else.
- Result never wraps to two lines; it auto-shrinks to fit.
- Last 10 previous results listed vertically under the result, no fade, never overlapping the bottom line (items that don't fit are hidden whole).

## Next
- Menu mode: pick an item off a menu.
