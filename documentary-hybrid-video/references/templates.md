# Templates — documentary-hybrid-video

Copy these shapes exactly. Chat messages stay short; every template below goes into a file/artifact.

## 1. Research brief (Stage 2) — `research_<slug>.md`

```markdown
# Research Brief: <topic-one-line>
Target <X:XX> | Language <lang> | Chapters <n> | A-roll via <phone/webcam/camera>

## Timeline of key events (with B-roll wishes)
| # | When | Where | What happened | Numbers/names | Card? | B-roll wish | Src |
|---|---|---|---|---|---|---|---|
| 1 | 26 Apr 1986, 01:23 | Reactor 4, Pripyat | ... | 203 crew | >> CARD: "01:23:44." | night plant wide shot / map push | [1] |

## Clipping-worthy quotes (exact wording + URLs, 8-12)
- "<exact sentence>" — <who/publication>, <date> [3]

## Conflicts & uncertainties
- Death toll: [2] says X, [5] says Y → on screen "<range, per [2][5]>"

## References
[1] <title> — <URL>
```

## 2. Blocking script (Stage 3) — `script_part<n>.md`

```markdown
# Part <n> — "<chapter title>" (target 0:00–6:10)

## BLOCK 12 — [A-ROLL] (est 0:31)
"Nobody asked why. I want you to understand today why nobody asked."
[look to camera last 2 s; hard cut on the exhale]
<!-- Lower third already used in Part 1; do not repeat -->

## BLOCK 13 — [VO-BROLL: map slow push, route Moscow→Pripyat] (est 0:24)
"The order left Moscow at 02:15 with one line of justification —"
[STAT BUG: '2,600 KM' while tracing route]

## BLOCK 14 — [CARD] (0:02)
>> CARD (L1): "ONE LINE. TWO WORDS. 'WE HAVE CONTROL.'"
(→ shorten to ≤5 words: "WE HAVE CONTROL.")
```

Rules: blocks 20-45 s; `[A-ROLL]` = face (stage directions in [brackets]), `[VO-BROLL: …]` = narration continues over visuals, `[CARD]` = full-screen typography; every card also logged in the Typography Plan.

## 3. Typography plan (attached to script)

```
 #   TIME   LEVEL  TEXT
 1   0:12   L1     "128 PEOPLE."
 2   0:47   L2     CH.1 — "WITHOUT A TRACE"
 3   1:05   L2.5   LOWER THIRD — "<NAME> — "<role>""
 4   1:31   L1     "3 HOURS OF FUEL LEFT."
```

## 4. Recording checklist (end of Stage 3)

```markdown
## A-roll recording checklist (Part <n>)
- Framing: face <left/right> third, eyes upper third, headroom 5-8%; clean third empty
- Light: window/key light on the face side; avoid backlit windows
- Audio: quiet room; phone 30-50 cm or cam mic; test 10 s first
- Per block: 3 s silence before + after; clap once at block start (sync aid)
- Watch [bracket] stage directions; do NOT say them aloud
- Files: aroll_part1.mp4, aroll_part2.mp4, ... (one per chapter, or one per block: block12.mp4)
- No A-roll yet? Say "continue" — timing generates from the script instead.
```

## 5. Timing sheet (Stage 4) — `timing.md`

```markdown
| Part | A-roll measured? | Blocks (in–out) | B-roll slots | Cards | Duration |
|---|---|---|---|---|---|
| 1 | yes (6:10 real) | b1 0:00–0:21 A | map 0:21–0:44 VO | #1 0:12 L1 | 6:10 |
| 2 | no (script est) | ... | ... | ... | 6:22 est |
Total: <X:XX> (target ±5%) | Cards re-timed with real values
```

## 6. Shot list (Stage 5) — `scenes_part<n>.md`

```markdown
| Shot | Block | In–Out | Ingredient | Visual | On-screen text (lvl) | Asset file | Fallback | Src |
|---|---|---|---|---|---|---|---|---|
| 7 | 13 | 0:44–0:49 | VO-BROLL | dashed route draw-on, IL-76 glyph leads | "2,600 KM" (L3.5 stat over map) | — | generated map | [1],[4] |
| 8 | 14 | 0:49–0:53 | CARD L1 | Guardian quote highlight, paper card, tilt 1° | "58 PASSENGERS." (L1) + SRC eyebrow | block14_guardian.png | animated clipping | [3] |
```

## 7. Asset checklists (Stage 5)

```
A-ROLL (required unless user chose continue-without)
 1. aroll_part1.mp4 — Blocks 1-9. Framing per checklist. If absent → script timing + silhouette fallback.
B-ROLL / ASSETS (upload block<NN>_<desc>.<ext> or say "use fallbacks")
 2. Required  block14_guardian.png  — screenshot, "58 passengers" line visible. Fallback: animated clipping [3]
 3. Optional  block09_plant_night   — archival night shot. Fallback: generated plant exterior stylized
 4. Optional  music_bed.mp3 — low documentary bed. Fallback: silent / generated pad
Royalty-free pool if wanted: Pexels, Pixabay, NASA archives, National Archives, Prelinger.
```

## 8. Chapter delivery note (Stage 6)

```
PART <n> — "<title>" (X:XX)
- Shots <m>: user assets <a> | generated <b> | placeholders <c> (list)
- Cards landed: #k @0:12 ✓ | #k+1 @0:47 ✓ | ...
- A-roll blocks: all landed / Block 12 missing → silhouette used
- RUN CARD: <current run card>
Changes? Applied to THIS part only.
```

## 9. RUN CARD (every chat deliverable)

```
TOPIC     : <one sharp line>
RUNTIME   : <target X:XX> | A-roll recorded <X:XX> | B-roll/scripts remaining <X:XX>
CHAPTERS  : <n> - <titles with timestamps>
A-ROLL    : <recorded : not yet> | <segments received: m/N>
AUDIO     : <A-roll internal mic/cam audio : separate VO : none yet> -> <timing source>
STAGE     : <current stage / what is required next from the user>
```

## 10. Missing-B-roll AI prompt (Stage 6, path 3)

```
SHOT 07 — 16:9, <DURATION s>
Subject & action: <precise, single action>
Camera: <shot size, angle, single move>
Lighting/style: "overcast practicals, desaturated, 35mm documentary still"
Negative: no text/logo/watermark, no identifiable real person
Slot: PLACEHOLDER_SHOT07.png
```
