---
name: documentary-longform-video
description: Produces presenter-free, long-form (8-30 min) YouTube documentary videos - cinematic map animations, chapter structure, and periodic full-screen kinetic typography "impact cards" (chapter titles, big dates, big numbers, quotes) with a strict typography hierarchy. Self-sufficient on audio: uses the user's MP3/WAV + SRT when provided, otherwise generates its own timing (TTS if available, otherwise a word-count timing sheet) so voiceover files are never a blocker. Staged workflow: brief, cited research, script + typography plan, timing, scene plan with asset request, then render. Use when the user wants a long documentary-style or history/geopolitics explainer video, a map-animation video, or says "start a documentary video".
---

# Documentary Long-Form Video

Produce an animated, **presenter-free** long-form YouTube documentary in the style of modern history/geopolitics channels: 3D-style map animations, animated routes and moving objects (planes, ships, vehicles), date/time stamps, highlighted "Source:" clippings, diagrams and cutaways - and above all a rhythm of **periodic big-text typography moments** that carry the story when narration alone would lose the viewer.

Two non-negotiables of this skill:

1. **Typography is a storytelling layer, not decoration.** Every 40-60 seconds something big hits the screen full-frame. The hierarchy below defines exactly how.
2. **Audio never blocks the pipeline.** If the user supplies MP3/WAV (+ SRT), the voiceover is the timing source of truth. If they do not, continue anyway with the skill's own timing generation (Stage 4). Never stop a project waiting for audio files.

Companion files (read them when a stage needs their detail):
- `references/style_guide.md` - exact palette, fonts, card anatomy, motion timings, map style, thumbnail spec
- `references/templates.md` - copy-paste output formats for every stage (research brief, script beats, typography plan, shot list, asset checklist, timing sheet, SRT note)

## Core rules

- Work in the six stages. Finish one, then **stop and wait**, except where a stage says to continue.
- Never start rendering before the script and scene plan are approved and assets are supplied or waived ("use fallbacks").
- Facts on screen must match the research and its citations. Never invent facts, quotes, numbers, or realistic images of real people.
- Keep chat messages short. Long content (research brief, script, shot list) goes into files or artifacts.
- Every deliverable carries a **RUN CARD** (see below) so the user always knows the topic and how much time is left / how long each section runs.
- If something is not possible in the current environment, say so plainly and offer the closest alternative, then continue.

### RUN CARD (attach to every chat deliverable)

```
TOPIC     : <one sharp line>
RUNTIME   : <target X:XX> | written so far <X:XX> | remaining <X:XX>
CHAPTERS  : <n> - <list of chapter titles with timestamps>
AUDIO     : <user MP3+WAV+SRT : yes/no> -> <timing source>
STAGE     : <current stage / what is required next from the user>
```

---

## The Look: typography & hierarchy system

Design language: dark cinematic background (near-black `#0B0D10`), one accent color (default deep red `#D6293A`; a map-blue `#2F7FE0` for data), high-contrast off-white text `#F4F1EA`. Fonts: a heavy display face (e.g. Archivo Black / Bebas Neue) for cards, a clean grotesque (e.g. Inter) for narration text and labels, monospace (e.g. IBM Plex Mono) for time stamps and source credits. All sizes below are for 1920x1080; scale proportionally.

**Hierarchy (biggest to smallest):**

| Level | Element | Size (px) | Style rules |
|---|---|---|---|
| 1 | IMPACT CARD - full-screen big text | 140-200 | One phrase/number/date per card, max 5 words, accent color on the key word, letter-spaced, subtle scale-in (0.35 s) + hold 1.5-2.5 s + fast exit |
| 2 | CHAPTER CARD - full-screen chapter opener | 96-120 | Chapter number small above (mono, 36 px), title huge below, 2-3 s hold, background dims 80% |
| 3 | KEY FACT CALLOUT - large text beside/below a map or diagram | 64-80 | Big number or date, underlined by a thin accent rule, animated count-up where numeric |
| 4 | NARRATION SUBHEAD - mid-screen supporting line | 48 | Sentence case, appears word-by-word (kinetic), synced to narration |
| 5 | LABELS / MAP ANNOTATION | 28-36 | City names, unit movements, arrows' captions |
| 6 | SOURCE CREDIT - corner clipping attribution | 22-26 | Monospace, 70% opacity, "SOURCE: <publication> <year>" |
| 7 | TIME-BURN - corner date/time stamp | 24-28 | Monospace, ticks forward during scene, always same corner |

**The 40-60 second rule:** scan the script beats; roughly every 40-60 s of runtime there must be at least one Level 1 or Level 2 moment at a natural story peak (a number, a date, a name, a turn in the story). Mark these in the script as `>> CARD: <text>` so the scene planner tiles them precisely. Two cards must never appear back-to-back.

**Impact card rules:** no sentence longer than 5 words; a number or a name is stronger than a phrase; use a period for finality, nothing for suspension ("3:47 AM" reads better than "The attack began at 3:47 in the morning").

---

## Stage 1: Brief + RUN CARD

Ask in one short message:
1. Topic (and the single most dramatic fact they already know about it)
2. Target duration: short form 8-12 min, standard 15-20 min, deep dive 25-30 min (16:9 YouTube; 9:16 only by explicit request)
3. Narration language (English / Hindi / Hinglish / Bangla / other)
4. Thumbnail too? (default: yes)
5. Audio workflow: "I will send MP3/WAV (+SRT)" **or** "self-voice it if possible / generate timing without audio" (default: generated timing - this keeps the project unblocked)

End Stage 1 by showing the first RUN CARD with the chosen topic and target runtime, plus a proposed 4-8 chapter spine (just titles + one line each). Then wait.

## Stage 2: Research with citations

Research via web search, favoring reliable sources (news archives, books, official records, reputable encyclopedias). Deliver a research brief as a file:
- A **timeline of key events**: dates, times, places, numbers, names - each entry tagged `>> CARD: <text>` if it deserves an impact card
- Inline numbered citations and a reference list with URLs
- Conflicting figures flagged, not silently resolved; uncertain points marked uncertain
- 8-12 "clipping-worthy" quotes/sentences with source URLs for on-screen "Source:" overlays

Update the RUN CARD (chapters may firm up here). **Continue to Stage 3 in the same reply** unless the topic clearly needs narrowing; then ask.

## Stage 3: Script + Typography Plan

Write narration sized to runtime using spoken words-per-minute: English 140-150, Hindi/Hinglish 130-150, Bangla 120-140. Format as numbered beats, each with:
- **Narration**: exactly what will be spoken
- **Visual**: map / object animation / clipping / diagram / dramatized scene
- **Sources**: citation numbers backing the beat
- `>> CARD:` lines wherever the 40-60 s rule demands a big-typography moment (Level 1 or 2), with the exact card text

Style: cold-open hook within the first 15 seconds (start in the middle of the most dramatic moment), suspenseful short sentences, specific dates/times/numbers, a chapter boundary every 4-7 minutes ending on a cliffhanger or a takeaway.

With the script, deliver the **Typography Plan**: the full list of Level 1/2 cards - `#, timestamp, card text, level` - so the user can see the rhythm of the big text at a glance, e.g.:

```
 1  0:12  CARD L1  "128 PEOPLE."
 2  0:47  CARD L2  CH.1 - "Without a Trace"
 3  1:31  CARD L1  "3 HOURS OF FUEL LEFT."
```

Ask the user to approve/edit the script and cards. Remind them: they may either record/generate the voiceover (MP3/WAV, one file per chapter - SRT welcomed but optional) **or** say "continue" and the skill generates its own timing. Wait.

## Stage 4: Timing (never a blocker)

Exactly one of three paths:

- **A. User supplied MP3/WAV + SRT** - the SRT is the timing source of truth. Report each chapter's exact duration and any script lines skipped/added/changed. Pause only if differences change an on-screen fact; otherwise continue.
- **B. User supplied MP3/WAV but no SRT** - transcribe with timestamps if the environment allows; otherwise ask for an SRT (Whisper / CapCut) once, and proceed with word-count timing estimates in the meantime so no work is wasted.
- **C. Nothing supplied** - continue automatically: script becomes the timing source. If TTS is available in the environment, synthesize narration per beat and use it. Otherwise build a **Timing Sheet**: each chapter = word count / WPM (+10% for pauses, breaths, card holds), per-beat start/end times, and card timings; total runtime stated with a ±5% tolerance. Render proceeds with silent or music-bed video and a note where the user's later audio can slot in - or the user's TTS-generated file drops in with zero retiming.

Report the final per-chapter durations and the updated full Typography Plan with real timestamps. **Continue to Stage 5** unless durations differ from target by more than 15%.

## Stage 5: Scene plan + asset request

Build a shot list timed to Stage 4, aiming for a new shot every 3-6 s, alternating map/data shots with scene shots, and tiling the Typography Plan cards exactly on the marked beats. Include: shot #, in/out time, shot type, on-screen text (level), sources.

Then a numbered **asset checklist**; for each item: what it is, which scene uses it, required or optional, and the fallback if not provided (animated text clipping, map, diagram, or generated scene). Typical assets: article screenshots, archival photos, photos of real people (never fabricated), logos, short B-roll clips, optional music. Name files by scene (`scene07_guardian.png`). Ask them to upload **or say "use fallbacks"** - fallback-only is a fully valid path that produces a complete video. Wait.

## Stage 6: Render

Before starting, ask once: burned-in captions (default: no) and background music (default: low documentary bed, if available or licensable).

Render **one chapter at a time** with text cards and animation synced to the Stage 4 timing:

1. **Python + ffmpeg available:** render the MP4. Draw maps from real geographic data (Natural Earth via geopandas/cartopy or simplified GeoJSON), animate with matplotlib/PIL frames or moviepy; composite user assets, kinetic text, clipping overlays; mux audio. Show each scene's first-frame preview before the full render when possible.
2. **Rendering not possible / output too large:** deliver a complete ready-to-render Remotion (React) project - one component per scene, card timestamps wired in, asset filenames wired in, plus exact commands (`npm install`, `npx remotion render`). Self-contained.
3. **Dramatized scenes:** where no image/video generation exists, write precise per-scene prompts for an external AI tool (subject, action, camera, lighting, style, aspect, duration) and leave a clearly marked placeholder slot.

After each chapter deliver: the video/project, a short scene list, which shots are generated vs. placeholders, the chapter's RUN CARD, and the card checklist confirming every Level 1/2 card landed. Ask for changes; apply changes to that chapter only. Then the next chapter.

**Thumbnail at the end:** bold 3-5 word title using the Level 1 type style, one dramatic key visual, the accent color from the style system, high contrast readable at 168 px wide.

## Quality gate before final delivery

- [ ] Every fact on screen has a citation number in the script
- [ ] Big-text rhythm: no 70 s gap without a Level 1/2 card, no cards back-to-back
- [ ] Typography hierarchy respected (seven levels, no invented sizes)
- [ ] Time-burn stamps correct and monotonic through each scene
- [ ] Chapter audio durations match the Timing Sheet / SRT within ±2 s
- [ ] All user assets attributed on screen by their source; nothing labeled "SOURCE:" that is not sourced
- [ ] Full RUN CARD with final runtime and chapter list delivered
