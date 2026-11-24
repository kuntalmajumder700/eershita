---
name: documentary-hybrid-video
description: Produces long-form (8-30 min) YouTube documentary videos in a HYBRID format - the user's facecam as A-roll presenter segments interleaved with B-roll (map animations, archival footage, clippings) and a full graphics layer (full-screen kinetic typography "impact cards", lower thirds, source clippings, time-burn stamps). Claude writes the presenter-ready blocking script with cue marks, the user records the A-roll, and Claude composites the edit. Timing is never a blocker - recorded A-roll is the source of truth, otherwise script-based timing. Staged workflow - brief/format, cited research, blocking script + typography plan, timing, scene plan with shot/asset checklists, render. Use when the user wants a presenter-style (facecam) documentary or hybrid explainer video, has facecam footage or will record it, or says "start a hybrid documentary video".
---

# Documentary Hybrid Video (Facecam A-Roll + B-Roll + Graphics)

Produce a long-form documentary where the **user is on camera (A-roll)** as the narrator, intercut with **B-roll** (3D-style map animations, animated routes, archival/stock clips, screencasts) and a **graphics layer** (full-screen kinetic typography cards, lower thirds, highlighted "Source:" clippings, time-burn stamps). Claude handles research, script, typography, editing decisions, and compositing; the user only records their facecam segments and drops files.

Two non-negotiables of this skill:

1. **The A-roll recording is the backbone.** The blocking script tells the user exactly what to say and when to leave their face so B-roll can take over. Once their footage arrives, it is the timing source of truth. If they have not recorded yet, continue anyway with script-based timing (Stage 4) - never block on footage.
2. **Graphics carry the rhythm.** Every 40-60 seconds something big hits the screen. Over the presenter's face we use lower thirds and side callouts; full-screen impact cards always fire over B-roll or a darkened background - text never fights the face for attention.

## Core rules

- Work in the six stages. Finish one, then **stop and wait**, except where a stage says to continue.
- Never invent facts, quotes, numbers, or realistic images of real people. Every on-screen fact traces to a citation.
- Keep chat short; long deliverables (research brief, script, shot list) go into files using `references/templates.md`.
- Every chat deliverable carries the **RUN CARD** so the user always knows topic, runtime, chapters, audio state, and stage.
- If something is not possible in the current environment, say so plainly and offer the closest alternative, then continue.

### RUN CARD (attach to every chat deliverable)

```
TOPIC     : <one sharp line>
RUNTIME   : <target X:XX> | A-roll recorded <X:XX> | B-roll/scripts remaining <X:XX>
CHAPTERS  : <n> - <list of chapter titles with timestamps>
A-ROLL    : <recorded : not yet> | <segments received: m/N>
AUDIO     : <A-roll internal mic/cam audio : separate VO : none yet> -> <timing source>
STAGE     : <current stage / what is required next from the user>
```

---

## Format anatomy (how the film is built)

The timeline alternates four ingredients:

1. **A-ROLL** - the user's facecam, in blocks of 20-45 s. Straight to camera, conversational energy. This is where authority and personality live.
2. **VO-BROLL** - the user keeps narrating (voice-over) while full-frame B-roll plays: map pushes, route animations, archival footage, clippings, dramatized shots. Most of the film's duration should live here - a good hybrid is ~30-40% face time.
3. **CARDS** - full-screen typography moments (Level 1/2) over B-roll or 80% darkened background.
4. **GRAPHIC OVERLAYS** - lower thirds and side callouts that live *over the A-roll* while the presenter keeps talking.

Cold open: start with VO-BROLL + an impact card (hook), then introduce the presenter via a lower third. Chapters end on a cliffhanger ON camera where possible (face = tension), and open with the chapter card.

## The Look: typography & hierarchy system

Design language: dark cinematic base (`#0B0D10`), ink `#F4F1EA`, accent `#D6293A` (drama/loss), accent-data `#2F7FE0` (facts/maps), paper `#E8E2D4` for clippings. Display face (Archivo Black/Bebas Neue) for cards, Inter for text/labels, IBM Plex Mono for stamps/credits. Exact colors, card anatomy, and motion timings: `references/style_guide.md`.

| Level | Element | Size (px, 1080p) | Where it lives |
|---|---|---|---|
| 1 | IMPACT CARD - full-screen big text | 140-200 | Only over B-roll/darkened bg; ≤5 words; scale-in 0.35 s, hold 1.5-2.5 s |
| 2 | CHAPTER CARD - full-screen chapter opener | 96-120 | Over dark bg; number small above (mono), title huge below |
| 2.5 | LOWER THIRD - presenter name/title chapter tag | 40-56 | Over A-roll, opposite third from the face, 2-3 s |
| 3 | KEY FACT CALLOUT | 64-80 | Over B-roll beside map/diagram; count-up if numeric |
| 3.5 | STAT BUG - corner callout over A-roll | 36-48 | Top-left box, "live fact" while presenter talks |
| 4 | NARRATION SUBHEAD (kinetic) | 48 | Over B-roll only, word-by-word synced |
| 5 | LABELS / MAP ANNOTATION | 28-36 | B-roll only |
| 6 | SOURCE CREDIT | 22-26 mono | On clip cards, 70% opacity |
| 7 | TIME-BURN date/time stamp | 24-28 mono | Fixed corner, any shot type |

**The 40-60 second rule:** at least one Level 1/2 card per 40-60 s at a story peak, never back-to-back, and always in a VO-BROLL stretch. Mark every card in the script with `>> CARD: <text>` / `[CARD: <text>]`.

**A-roll grammar:** cut on movement or a breath (jump cuts, not dissolves); punch-in to ~1.2x for emphasis moments; the face occupies the left or right third leaving the opposite third clean for lower thirds. Ken Burns (slow zoom) on any long static take.

---

## Stage 1: Brief + run card

Ask in one short message:
1. Topic (and the single most dramatic fact they already know)
2. Target runtime: 8-12 / 15-20 / 25-30 min (16:9 YouTube; 9:16 only by request)
3. Narration language (English / Hindi / Hinglish / Bangla)
4. **Recording setup**: phone / webcam / mirrorless camera; background = real room (framed for thirds) or green screen; which third should the face sit in, left or right
5. Thumbnail? (default yes)
6. B-roll policy: upload-own / royalty-free stock library / fallback-only (default: whatever is possible + fallbacks)

Show RUN CARD + proposed 4-8 chapter spine. Then wait.

## Stage 2: Research with citations

Web-research reliable sources. Deliver the research brief (`references/templates.md`) as a file: timeline table with `>> CARD:` tags, numbered citations + URLs, conflicts flagged, 8-12 clipping quotes, **and a B-roll wish list column** (what footage/diagram each beat wants). Update the RUN CARD. **Continue to Stage 3 in the same reply** unless the topic needs narrowing.

## Stage 3: Blocking script + Typography Plan

Write the script in **blocks of 20-45 s**, every block tagged with how it is delivered:

```markdown
## BLOCK 06 — [A-ROLL] (0:21)
"For twenty years we believed the fire crew knew what they were walking into."
[Hold last 2 s — deadpan. Cut here.]

## BLOCK 07 — [VO-BROLL: map slow push into Pripyat] (0:24)
"But the radio readings that night said otherwise —"
[LOWER THIRD: "26 April 1986 - 01:23" if first A-roll]

## BLOCK 08 — [CARD] (0:02)
>> CARD (L1): "3500 RÖNTGEN."
```

Rules: presenter lines are spoken text exactly as said (teleprompter-ready, sentence case, short); `[A-ROLL]` blocks carry stage directions in [brackets]; `[VO-BROLL: …]` says what plays while they keep narrating; `>> CARD:` marks full-screen typography. Hook within 15 s (VO-BROLL + card). Chapter boundary every 4-7 min, ending on camera (cliffhanger) or on a takeaway card. WPM for VO blocks: English 140-150, Hindi/Hinglish 130-150, Bangla 120-140; A-roll reads slightly faster naturally.

Attach the **Typography Plan** (#, timestamp, level, text) and a one-page **recording checklist** (framing, light, 3-second pre-roll silence per block, name files `aroll_partX.mp4`). Ask them to record each chapter's A-roll blocks and upload (cam audio is fine), or say "continue" for script-based timing. Wait.

## Stage 4: Timing (never a blocker)

- **A. A-roll footage received** - measure each block's duration; A-roll is the source of truth. Schedule B-roll and cards into the gaps and over the footage. Report per-chapter durations; pause only if a recorded change affects an on-screen fact.
- **B. Partial footage** - time what arrived, script-time the rest, flag the deltas.
- **C. Nothing recorded yet** - build the Timing Sheet (word count / WPM +10%, per-block in/out, card times, ±5%) so research/rendering never stalls; footage slots in later with zero retiming because blocks are independent.

Report final per-chapter durations + updated Typography Plan with real timestamps. **Continue to Stage 5** unless durations differ from target by >15%.

## Stage 5: Scene plan + asset request

Build the shot list (`references/templates.md`): every block mapped to its ingredient (A-ROLL / VO-BROLL / CARD / OVERLAY), in-out times, on-screen text level, sources. Aim: a new visual every 3-6 s during VO-BROLL, no >70 s gap without a Level 1/2 card.

Then numbered checklists:
1. **A-roll checklist** - which blocks still need recording, file naming, the one-page framing/ǪA list
2. **B-roll / asset checklist** - each item: what, which block, required/optional, fallback (animated map, diagram, stylized stock, typographic scene). Suggest royalty-free sources when allowed (Pexels/Pixabay/NASA/National Archives/public domain). User uploads `block<NN>_<desc>.<ext>` or says **"use fallbacks"** - a fully valid path to a complete video.

Wait.

## Stage 6: Render / composite

Ask once: burned-in captions (default no), background music (default low documentary bed, ducked -6 dB under speech and cards).

Composite **one chapter at a time**:

1. **Python + ffmpeg available:** cut A-roll (remove dead takes, jump cuts on breaths), lay VO-BROLL under narration audio, key out green screen if provided (or vignette/matte the room bg), overlay the graphics layer per the plan, add captions/credits, mux audio, gentle grain + vignette 15% across the film. Show first-frame previews per scene when possible.
2. **Rendering not possible / output too large:** deliver a complete self-contained Remotion (React) project - `ARollClip`, `BrollClip`, `ImpactCard`, `LowerThird`, `TimeBurn` components; per-block durations wired from Stage 4; asset filenames wired; exact `npm install` / `npx remotion render` commands.
3. **Missing B-roll:** generate what is possible (maps from Natural Earth/GeoJSON, diagrams, kinetic typography scenes) and write precise AI-image/video prompts for the rest, leaving marked placeholder slots.

After each chapter: the cut, a short scene list (generated vs. user vs. placeholder), cards-landed check, RUN CARD. Revisions touch that chapter only. Next chapter.

**Thumbnail at the end:** presenter's real face (never fabricated) + 3-5 word Level 1-style title + one accent-colored key element; readable at 168 px.

## Quality gate before final delivery

- [ ] Every on-screen fact has a citation number
- [ ] Face time 30-40% (±10%); no silent-or-static A-roll stretch >45 s unbroken
- [ ] Big-text rhythm: no 70 s gap without a Level 1/2 card, never back-to-back, never over the face
- [ ] Lower thirds/stats only in the clean third; time-burn monotonic
- [ ] Cuts on breath/movement, no mid-word jump cuts
- [ ] Audio: speech peaks -6 to -3 dB, bed ducked -6 dB under speech, no clipping
- [ ] Chapter durations match Stage 4 within ±2 s
- [ ] Final RUN CARD with full chapter list delivered
