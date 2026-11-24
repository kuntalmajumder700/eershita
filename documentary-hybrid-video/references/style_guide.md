# Style Guide — documentary-hybrid-video

Visual language for the hybrid format (facecam A-roll + B-roll + graphics). The 7-level hierarchy lives in `SKILL.md`; this file defines exact look, motion, and the presenter-side rules.

## 1. Palette

| Token | Hex | Use |
|---|---|---|
| `bg` | `#0B0D10` | Base background, cards, darkened A-roll underlays |
| `bg-raised` | `#151921` | Panels, stat bug, clip backing |
| `ink` | `#F4F1EA` | Primary text, warm off-white |
| `ink-dim` | `#9AA0A8` | Secondary labels (70-90% opacity use) |
| `accent` | `#D6293A` | The single drama accent: key word on cards, danger/loss |
| `accent-data` | `#2F7FE0` | Facts/maps only: big numbers, routes, measurements |
| `paper` | `#E8E2D4` | Source clipping backgrounds |

One accent strong per scene: red = human cost/danger, blue = neutral number/measurement.

## 2. Typography

- **Display** (cards, chapter titles): Archivo Black or Bebas Neue. UPPERCASE L1/L2, tracking +4-8%.
- **Text** (lower thirds, subheads, labels): Inter. Weight 600 for lower thirds, 500 subheads, 400-500 labels.
- **Mono** (time-burn, credits): IBM Plex Mono / JetBrains Mono, 70-90% opacity.
- Bangla narration text: Noto Sans Bengali; kinetic subhead lines ≤ 32 chars.
- Numerals: tabular figures on cards and stat bugs.

## 3. Articulation anatomy

**Impact card (L1):**
```
[ eyebrow: 14px mono, ink-dim — "DAY 14 — APRIL 26" ]
[ THE TEXT: 140-200px, ink; ONE key word/number in accent ]
[ underline rule: 2-3px accent, 60% of text width ]
```
≤5 words, one idea. Number or name beats phrase. Compose centered, or bottom-belt over a dimmed map.

**Chapter card (L2):** bg dims to 80%; chapter number mono 36px fades in, then title 96-120px; hold 2.5-3 s.

**Lower third (L2.5, over A-roll):** solid `bg-raised` bar (opacity 92%), 6px accent left rule; two lines max — name/unit (Inter 600, 40-48px) + subtitle (Inter 400, 24-28px, ink-dim). Slides in 0.3 s from the clean third, holds 2.5-3 s, slides out 0.25 s. Never covers the face, never over a jump cut.

**Stat bug (L3.5, over A-roll):** top-left pill, `bg-raised` 90%, label mono 20px + value 36-48px in `accent-data`; ties to the exact narration word (in 0.2 s before, out 0.3 s after the sentence).

**Source clipping:** `paper` bg card, drop shadow 20%, headline display 40-56px, key sentence accent-underlined, eyebrow "SOURCE: <PUBLICATION> — <YEAR>" mono 22-26px at 70%, tilt ≤1°.

## 4. Motion rules

| Element | In | Hold | Out |
|---|---|---|---|
| Impact card | 0.35 s scale 0.94→1.0 + 12px rise | 1.5-2.5 s | 0.2 s fade / 0.25 s snap-down |
| Chapter card | 0.5 s dim + staggered title | 2.5-3 s | 0.4 s cross-fade |
| Lower third | 0.3 s slide from clean third | 2.5-3 s | 0.25 s slide |
| Stat bug | 0.2 s | tied to sentence | 0.3 s |
| Kinetic subhead | 60-90 ms/word | — | 0.2 s fade |
| Map camera | constant slow drift (8-15 px/min @1080p) | — | hard cuts between scenes |
| Route draw-on | 0.8-1.5 s + leading dot/vehicle | — | — |

Text may lead its narration word by 0-100 ms, never more. No bounce, no rubber-band, no glow.

## 5. A-roll presentation rules (the human layer)

- **Framing:** face in left or right third (as decided in Stage 1), eyes on upper-third line; ~30% of frame width. The opposite third stays clean for lower thirds. Headroom 5-8%.
- **Backdrop:** real room → everything behind the clean third must be simple/dark (a wall, one plant max) or we matte/vignette it. Green screen → key only if lighting is clean; else we vignette + darken 20%.
- **Editing the human:** cut on breaths or gesture starts; jump cuts only (plus optional 0.2 s white-flash accent on big turns); punch-in 1.2x on emphasis; slight Ken Burns (1.02→1.05 over the take) keeps static takes alive.
- **Color on the face:** neutral grade, natural skin; grade only the B-roll layers. Face and B-roll must not battle — B-roll is slightly cooler/desaturated next to neutral skin.
- **Audio:** cam audio acceptable; normalize speech peaks to -6…-3 dB; de-noise if hum, never over-process. Room tone matched across blocks.
- **Fallback face-visual:** if a block wasn't recorded but VO exists → stylized silhhouette frame + larger kinetic subtitles + note in the delivery list.

## 6. Screen furniture

- **Time-burn (L7):** bottom-right `DAY 01 — 03:47 LT`, ticks in scene, resets per scene, all shot types.
- **Captions (optional):** bottom-center, Inter 42px, bg pill 60% black, off when a card is up.
- **Grain/vignette:** 3-5% grain + 15% vignette, constant, both layers (tie layers together).
- **Matte borders:** 5% safe margins for L1-4 text.

## 7. Pacing & sound

- New visual every 3-6 s during VO-BROLL; within one B-roll idea, camera drift counts as continuity.
- Card rhythm: ≥1 L1/L2 per 40-60 s; never two in a row; always in a VO-BROLL stretch.
- Chapter in: 0.6 s black → chapter card. Chapter out: end the cliffhanger ON camera, cut to black 0.4 s after the last word.
- Music: minimal percussive bed -18…-22 dB under speech, -6 dB duck when presenter speaks or a card holds; optional 0.8-1.2 s riser before chapter-end cliffhangers.

## 8. Thumbnail spec

1280×720, readable at 168 px: presenter's real face cropped tight (never fabricated), facing the title, 3-5 word Level-1-style title (≤4 lines), one accent-colored key element/map fragment, high contrast.
