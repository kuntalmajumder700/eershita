# Style Guide — documentary-longform-video

The complete visual language for every rendered frame. The main `SKILL.md` defines the hierarchy; this file defines the exact look, motion, and pacing rules. If anything conflicts, `SKILL.md` wins.

## 1. Palette

| Token | Hex | Use |
|---|---|---|
| `bg` | `#0B0D10` | Base background, near-black |
| `bg-raised` | `#151921` | Panels, clip-card backing |
| `ink` | `#F4F1EA` | Primary text, warm off-white |
| `ink-dim` | `#9AA0A8` | Secondary labels, 65-75% opacity equivalents |
| `accent` | `#D6293A` | The one accent: keywords on cards, route lines, danger/loss |
| `accent-data` | `#2F7FE0` | Data/maps only: numbers, arrows, measurements |
| `paper` | `#E8E2D4` | Source clipping backgrounds (aged paper look) |

Rules:
- Exactly one accent dominates a scene. `accent` (red) = human cost, danger, drama; `accent-data` (blue) = neutral fact/measurement. Never use both at full strength in the same shot.
- Background never pure black; text never pure white.

## 2. Typography

- **Display** (cards, titles): Archivo Black or Bebas Neue. UPPERCASE for Level 1/2, tracking +4-8%.
- **Text** (narration subheads, labels): Inter (or Roboto). Sentence case, weight 500-600 for subheads, 400-500 for labels.
- **Mono** (time-burn, source credits, coordinates): IBM Plex Mono or JetBrains Mono. Always slightly translucent (70-90%).
- Never mix two display faces. Numerals on impact cards prefer tabular figures.
- Bangla narration text: Noto Sans Bengali; keep Level 4 line-length ≤ 32 characters.

## 3. Articulation (Level 1/2 card anatomy)

A full-screen impact card has exactly three zones:

```
[ optional eyebrow: 14px mono, ink-dim, e.g. "DAY 14 - APRIL 26" ]
[ THE CARD TEXT: 140-200px display, ink; the single key word/number in accent ]
[ optional underline rule: 2-3px, accent, 60% of text width ]
```

- Word cap: 5. One idea per card. A number or name beats a phrase.
- Compositions: centered (default), left-third (when a map edge remains visible behind at 40% dim), or bottom-belt for numbers over a dimmed map.
- Over a moving map: dim the map to 40-55% under the card; never run full-brightness text over full-brightness detail.

## 4. Motion rules

| Element | In | Hold | Out |
|---|---|---|---|
| Impact card | 0.35 s scale 0.94→1.0 + 12px rise, ease-out | 1.5-2.5 s | 0.2 s fade or 0.25 s snap-down; never both slow |
| Chapter card | 0.5 s: bg dims to 80%, number fades in, title follows 0.15 s later | 2.5-3 s | 0.4 s cross-fade into scene |
| Key fact callout | 0.3 s slide from left; numeric count-up over 0.8 s where numeric | until narration point passes | 0.2 s fade |
| Kinetic subhead | word-by-word, 60-90 ms per word, synced to narration | — | 0.2 s fade |
| Map camera | slow drift always (8-15 px/min zoom or pan at 1080p); hard cuts only between scenes | — | — |
| Route animation | 0.8-1.5 s draw-on with a small leading dot or vehicle glyph | — | — |

- Nothing enters before its narration word: text leads audio by 0-100 ms, never more.
- No bounce, no rubber-band, no glow. Motion is documentary, not marketing.

## 5. Screen furniture

- **Time-burn** (Level 7): bottom-right, fixed, `DAY 01 - 03:47 LT` format, ticks within scenes, resets per scene. Never overlaps narration subhead.
- **Source clipping** (Level 6 + `paper`): a rectangular card styled like a print clip, drop shadow 20% black, headline in display face 40-56px, key sentence highlighted with accent marker, credit eyebrow "SOURCE: THE GUARDIAN - 2014". Tilt 0.5-1.5° max, never more.
- **Map style**: landmass `#1A2029`, borders `#39424E`, labels `ink-dim`, routes/animated objects in `accent` or `accent-data`, flat 2.5D look (subtle vertical extrusion on landmass edge, 6-10 px).
- **Grain/vignette**: 3-5% film grain overlay, soft vignette 15% — both constant through the whole film.
- **Safe margins**: 5% all sides; never place Level 1-4 text outside them.

## 6. Pacing & sound

- New shot every 3-6 s. A map shot is followed by a non-map shot whenever possible.
- Chapter boundary: end previous chapter 0.5 s before the cliffhanger word, then hard cut to black for 0.6 s, then chapter card.
- Music bed: low, percussive-minimal documentary bed at -18 to -22 dB under narration; duck -6 dB under impact cards; no music under Level 1 cards if the track has vocals.
- Optional subtle riser (0.8-1.2 s) before a chapter-ending card, out with the cut.

## 7. Thumbnail spec

- 1280×720, readable at 168 px wide.
- Level 1 type style for a 3-5 word title (≤ 4 lines), one dramatic key visual, `accent` as the single strong hue, subject cropped tight, eyes/actors facing the title.
- Face of real people only if a real verified photo exists (never fabricated); otherwise map + symbolic object.
