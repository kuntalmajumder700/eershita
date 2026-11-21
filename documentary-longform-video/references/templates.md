# Templates — documentary-longform-video

Output formats for every stage deliverable. Copy these shapes exactly; keep file deliverables in files/artifacts, not in chat.

## 1. Research brief (Stage 2) — `research_<slug>.md`

```markdown
# Research Brief: <topic-one-line>

## Target
Runtime <X:XX> | Language: <lang> | Chapters: <n>

## Timeline of key events
| # | When (as precise as possible) | Where | What happened | Numbers/names | Card-worthy? | Src |
|---|---|---|---|---|---|---|
| 1 | 26 Apr 1986, 01:23 | Reactor 4, Pripyat | ... | 203 crew on shift | >> CARD: "01:23:44." | [1] |

## Clipping-worthy quotes (for "Source:" overlays)
- "<exact sentence>" — <who/publication>, <date> [3]
(8-12 entries, exact wording, with URLs)

## Conflicts & uncertainties
- Death toll: source [2] says X, source [5] says Y -> on screen use "<range, per [2][5]>"

## References
[1] <title> — <URL>
```

## 2. Script beat (Stage 3) — `script_part<n>_<slug>.md`

```markdown
# Script Part <n> — "<chapter title>" (target 0:00-6:20)

## Beat 7
**Narration**: "At 01:23, the shutdown button went in. Ninety seconds later, the roof was gone."
**Visual**: map, slow push into Reactor 4; time-burn resets
**Sources**: [1], [4]
>> CARD (L1): "90 SECONDS."
```

Rules recap: `>> CARD:` on the beat where it fires (L1 = impact card, L2 = chapter card); 140-150 wpm English, 130-150 Hindi/Hinglish, 120-140 Bangla; chapter boundaries end on a cliffhanger/takeaway.

## 3. Typography plan (attached to the script)

```
 #   TIME   LEVEL  TEXT
 1   0:12   L1     "128 PEOPLE."
 2   0:47   L2     CH.1 — "WITHOUT A TRACE"
 3   1:31   L1     "3 HOURS OF FUEL LEFT."
```

## 4. Scene plan / shot list (Stage 5) — `scenes_part<n>.md`

```markdown
| Shot | In–Out | Type | On-screen text (level) | Visual detail | Assets | Src |
|---|---|---|---|---|---|---|
| 7 | 0:44–0:49 | map-route | "2,600 km" (L3) | dashed route Moscow→Chernobyl draws on, IL-76 glyph leads | — | [1],[4] |
| 8 | 0:49–0:53 | clipping | card text (L1) | Guardian quote highlight, paper card, tilt 1° | scene08_guardian.png (opt; fallback: animated clipping) | [3] |
```

## 5. Asset checklist (Stage 5)

```
 1. Required  scene08_guardian.png — Guardian article screenshot, "58 passengers" line visible.  Fallback: animated text clipping from quote bank [3]
 2. Optional  scene12_plane.png — IL-76 photo for cutaway.                  Fallback: labeled schematic silhouette
 3. Optional  music_bed.mp3 — low documentary bed.                          Fallback: silent / generated ambient pad
```

File naming: `scene<NN>_<source>.<ext>`, one file per scene, NN = first shot using it.

## 6. Timing sheet (Stage 4, path C) — `timing.md`

```markdown
| Part | Words | WPM | +pauses | Duration | In–Out |
|---|---|---|---|---|---|
| 1 | 812 | 145 | +10% | 6:10 | 0:00–6:10 |
| Beats within part 1: b1 0:00–0:09 | b2 0:09–0:21 | ... |
| Cards re-timed: #1 0:12 | #2 0:47 | #3 1:31 |
Total: 18:42 (target 18:00, tolerance ±5% OK)
```

## 7. Voiceover request (end of Stage 3, only if path A/B)

```
Please record or generate one audio file per part:
  part1.mp3, part2.mp3, ...
Name them exactly like this. SRT welcomed but optional
(e.g. from Whisper:  whisper part1.mp3 --output_format srt ).
No audio yet? Say "continue" and I will generate the timing myself.
```

## 8. Chapter delivery note (Stage 6, per part)

```
PART <n> — "<title>" (duration X:XX)
- Shots: <m> total | generated <a> | placeholder <b> (list)
- Cards landed: #k @0:12 ✓ | #k+2 @0:47 ✓ | ...
- RUN CARD: <current full run card>
Changes? I will edit THIS part only and keep the rest identical.
```

## 9. RUN CARD (every chat deliverable)

```
TOPIC     : <one sharp line>
RUNTIME   : <target X:XX> | written so far <X:XX> | remaining <X:XX>
CHAPTERS  : <n> - <titles with timestamps>
AUDIO     : <user MP3+WAV+SRT : yes/no> -> <timing source>
STAGE     : <current stage / what is required next from the user>
```

## 10. Dramatized-scene prompt (Stage 6, path 3)

```
SCENE 14 — 9:16/16:9, <DURATION s>
Subject & action: <precise, single action>
Camera: <shot size, angle, single move>
Lighting/style: <e.g. "overcast practicals, desaturated, 35mm documentary still">
Negative: no text/logo/watermark in frame, no identifiable real person
Slot in project: PLACEHOLDER_SCENE14.png
```
