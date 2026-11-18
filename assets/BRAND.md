# KX Game Studios

KX Game Studios is a two-person game studio run by Alek and Alex. The names differ by one letter, K and X, and the logo locks those two letters together: two folded ribbons form the K and the X, and the diamond they enclose holds a cut gem. The gem is the thing every game hides somewhere for the player to find.

## Logo

- **Mark**: the interlocked KX with the gem. Two ribbons, each folded once: one runs from the K up over the top and down through the X, the other mirrors it underneath. They cross once, with a thin over-under gap.
- **Stacked logo**: mark above the wide-tracked wordmark. The default.
- **Horizontal logo**: mark beside a two-line wordmark, for headers and store pages.
- **Emblem**: the mark on a cut-corner purple tile, for avatars, badges and merch.
- **Gem**: the gem on its own, for bullets, loading states, achievements and favicons at tiny sizes.

The wordmark letters are custom drawn: one stroke weight, flat ends, corners cut at 45 degrees. Do not retype the name in a font and call it the logo.

Rules:

- On dark and purple grounds the ribbons are `white` with `purple-light` folds. On light grounds they are `purple` with `purple-shade` folds. The gem keeps its five facet colours everywhere.
- Mono marks (`kx-mark-mono-white`, `kx-mark-mono-black`) are for photos, engraving and one-colour print.
- Keep clear space equal to the width of the K stem on all sides. Minimum width: mark 48px, stacked logo 140px. Below that, use the gem alone.
- Do not recolour the gem, flatten the folds in the colour versions, outline, rotate, stretch or add glows and gradients.

## Colour

Dark first. Purple leads, the gem colour is the accent, black and white carry the rest.

| Token | Value | Role |
| --- | --- | --- |
| `purple` | #6C2BD9 | Primary. Ribbons, emblem, primary buttons. |
| `gem` | #2FE0D2 | Secondary. The gem, highlights, one call to action per view. |
| `bg` (dark) | #120A24 | Default ground, a violet-black. |
| `white` | #FFFFFF | Ribbons on dark, text on purple and dark. |
| `black` | #0E0B14 | Text on light grounds and on `gem`. |
| `purple-deep` | #2A0F5C | Hero grounds, pattern on purple. |

Gem facets, lightest to darkest: `gem-glint` #C9FBF6, `gem-light` #7FF0E8, `gem` #2FE0D2, `gem-shade` #19BDB2, `gem-deep` #0F9C94.

Aim for roughly 60% dark ground, 30% `purple`, 10% `gem`. Text on `purple` is `white`; text on `gem` is `black`, never white. For small coloured text use `purple-text` and `gem-text`, which shift per theme to stay readable.

## Type

- **Chakra Petch** (Google Fonts, 600 and 700) for titles, buttons and labels. Its squared, cut-corner shapes echo the wordmark.
- **DM Sans** (Google Fonts, 400 and 500) for body text.

Titles are sentence case. Labels and buttons are uppercase with 0.08em tracking (`label`).

## Shape and pattern

Everything sits on a 45 degree grid. Corners are square or cut, never pill shaped: `radius-none` by default, `radius-md` at most. The pattern is a thin diamond lattice in `line` with a few small gems and four-point sparkles dropped into cells. Use it on banners, loading screens and packaging, not behind body text. Sparkles are `white` or `purple-text`, never more than one per four cells.

## Voice

Short and direct, like good tutorial text. Say what the game is and what the player does. No hype words, at most one exclamation mark per page.

- Yes: "A two-player puzzle game about sharing one controller."
- No: "An epic, groundbreaking co-op experience!"

## Files

- `assets/Logos`: marks, logos, emblem, gem and wordmarks as SVG.
- `assets/Icons`: full-bleed app icon as SVG and PNG (512, 192, 32).
- `assets/Graphics`: tileable lattice patterns and a 1500 x 500 social banner.
