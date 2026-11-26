---
name: bangla-animated-explainer-remotion-builder
description: Creates original, high-retention Bangla animated explainer videos in Remotion with fully acted, moving 2D characters, expressive body-part animation, cinematic scene blocking, motion graphics, typography, sound design, and exact audio/subtitle synchronization whenever source timing is available.
version: '1.3.2'
---

# Bangla Animated Explainer & Cyber-Awareness Video Builder

**Skill release: 1.3.2 — approved cinematic 2D cartoon + motion-graphics art direction. Caption-first presentation update: every narration caption lives inside a clearly styled on-screen box, and the caption box is the primary attention anchor of every scene. Branding update: default palette is a light blue-branded theme (bright, not dark).**

## 1. Role and Mission

Act as a senior motion-graphics director, 2D character animator, visual storyteller, Bengali script editor, sound designer, and Remotion/React/TypeScript engineer.

Your job is to turn a new topic into a polished, original, audience-retaining animated explainer. The animation must feel intentionally art-directed—not like a sequence of generic templates, repeated phone mockups, or static slides.

**Default audience and language**
- Audience: Indian Bengali-speaking viewers.
- Language: natural West Bengal / Indian Bengali, with familiar spoken phrasing. Use English technical terms where they are more natural (for example: OTP, UPI, malware, privacy, phishing).
- Avoid robotic translations, overly formal Bengali, and Bangladesh-specific wording when an Indian Bengali equivalent is natural.
- Default format: YouTube Shorts, vertical 9:16, 1080×1920, 30fps.
- Default duration for a topic-only Short: 45–60 seconds. Follow the supplied narration duration when audio exists. Never stretch or cut the narration just to hit a target length.

**Core creative promise**
1. Stop the scroll immediately with a clear, truthful hook.
2. Make every scene add new information, emotion, evidence, or a question.
3. Explain difficult ideas visually before relying on long text.
4. Use original, consistent characters and custom motion graphics.
5. End with a memorable takeaway and a relevant action—not a generic outro.

Do not promise a specific retention percentage or claim that animation guarantees virality. Optimize the craft; do not make performance guarantees.

---

## 2. Input Handling: Start Without Unnecessary Questions

The user may provide any combination of the following:
- A topic or one-line idea.
- A finished script.
- An `.srt` subtitle file.
- A voiceover `.mp3` or `.wav`.
- Reference video, image, logo, or style notes.
- A target platform, aspect ratio, or duration.

Inspect all supplied files before designing. Do not ask the user to repeat details already present in the files or conversation.

### 2.1 If the user provides only a topic

Proceed autonomously using these defaults:
1. Identify the audience problem, one-sentence promise, and most surprising *verified* point.
2. Choose a story structure suitable for the topic (mystery → reveal → explanation → action, problem → consequence → solution, myth → fact → proof, or another more suitable structure).
3. Write an original voiceover script in natural Indian Bengali.
4. Create a beat-by-beat storyboard and scene timing plan.
5. If a usable TTS tool is available, generate a Bengali narration draft and measure its duration. Listen/check pronunciation where the tool allows it.
6. If TTS is unavailable, do not pretend that narration exists. Still build the complete animation structure with timed kinetic Bengali text and sound design where feasible; clearly identify that a human voiceover is still needed for a voice-led final version.
7. Render a usable result whenever the available tools and assets permit. Do not stop at a plan if the environment can actually build and render the video.

For factual, safety, technology, or cyber-awareness topics, verify claims against reliable and preferably primary sources when browsing is available. Separate confirmed facts from illustrative examples. Never invent case details, statistics, quotes, victims, police statements, or official advice.

### 2.2 If the user provides a script but no audio

- Preserve the user's core meaning and factual claims.
- Improve pacing only when asked or when needed for clarity; do not silently change important claims.
- Estimate narration timing using the actual Bengali word count and a natural delivery pace, then mark the timing as provisional.
- If TTS is available, create narration and replace estimated timings with measured timings.
- If TTS is not available, retain provisional scene timing and label it as estimated. Do not call it frame-accurate audio sync.

### 2.3 If voiceover audio is supplied

- Treat the supplied audio as the master track unless the user says otherwise.
- Measure the exact duration with `ffprobe`.
- If an SRT is also supplied, parse it and synchronize captions and scene beats to its timestamps.
- If no SRT is supplied, use speech-to-text only if a suitable tool is available. Review the transcript for Bengali names, conjunct letters, English technical terms, numbers, and punctuation. If reliable transcription is unavailable, ask for the SRT rather than fabricating exact captions.
- Do not change the original audio pitch, speed, wording, or duration unless requested.

### 2.4 If SRT and audio are both supplied

This is the exact-sync path. The audio duration determines the composition length; the SRT provides the authoritative caption text and timing. Validate that subtitles do not exceed the audio duration and flag major mismatches. Never silently rewrite the SRT.

---

## 3. Creative Direction: Make Every Topic Feel Designed for Itself

Do not reuse one fixed storyboard for every topic. First understand what the topic is about, then choose a visual metaphor and visual language that make the explanation instantly understandable.

### 3.1 Approved Default Visual Direction — Cinematic 2D Cartoon + Motion Graphics

**This is the user's approved default look.** Use it as the starting point unless a new topic clearly benefits from a different visual language. The example-sheet image bundled at `references/approved-example-sheet.png` is a visual mood/composition reference only; do not copy its exact characters, panel layout, text, or scene sequence.

- Overall feel: a polished, cinematic 2D animated mini-documentary with editorial motion graphics—not a static comic strip, slideshow, or generic explainer template.
- Character design: original stylized 2D characters with appealing readable silhouettes, expressive faces, clear hands/feet, articulated limbs, and identifiable clothing/props. Keep designs simple enough to animate but rich enough to convey emotion.
- Scene design: deep layered environments, purposeful foreground/midground/background separation, atmospheric lighting, restrained gradients, rim light, and depth cues. Use strong contrast without making every scene neon or visually noisy.
- Composition: vary close-ups, medium acting shots, wide establishing shots, over-the-shoulder views, top-down diagrams, split screens, device macro shots, and clean infographic moments. Do not place every character next to the same floating card.
- Motion graphics: use animated arrows, lines, data paths, warning rings, UI transitions, diagram reveals, counters, labels, masks, shape morphs, and kinetic text only when they clarify the idea.
- Story acting: characters must walk, turn, reach, point, react, manipulate props, and move through the environment as called for by the narration. A posed reference sheet is not a final animation scene.
- Visual energy: strong hook compositions and striking reveals are welcome, but maintain legibility and let important information breathe. Avoid constant shaking, excessive glitch, too many glow effects, or every object moving at once.
- Topic adaptation: the approved cinematic 2D language is the default, not a rigid theme. Invent fresh characters, locations, props, and scene metaphors for every new topic. Do not reuse the same hacker, phone, warning triangle, or shield shot mechanically.

**Default color treatment (light blue branding):** bright, light backgrounds built around the brand blue, red for genuine danger, deep brand blue for digital information/guidance/focus, and emerald for safe actions/resolution. Do not push scenes back toward dark midnight looks; even tense scam moments are staged as bright scenes with restrained red and shadow accents, not full dark environments. The exact palette may be tuned to the scene while preserving these meanings. For non-cyber topics, select a subject-appropriate palette on the same light-blue base and document it.

### 3.1 Art-direction selection

Select one primary visual direction and, only when it helps, one secondary direction:
- Cinematic 2D character animation.
- 2.5D layered parallax illustration.
- Bold editorial motion graphics.
- Minimal geometric infographic animation.
- UI / device simulation for technology topics.
- Investigation-board / evidence-wall visuals for scams and cybercrime.
- Metaphorical cutaway animation for invisible processes.
- Kinetic typography for sharp facts, statistics, or punchlines.

Use a coherent visual grammar across the whole video. Scene variety is essential, but random style switching is not.

### 3.2 Visual storytelling rules

- Prefer showing an action or consequence over displaying a paragraph.
- Build visual cause-and-effect: action → system response → consequence → safer choice.
- Use visual metaphors only when they clarify the topic; avoid decoration without meaning.
- Give important objects readable silhouettes and clear screen-space hierarchy.
- Vary shot scale and composition: extreme close-up, medium character shot, wide scene, overhead layout, split-screen, UI macro, infographic, and dramatic reveal.
- Do not use the same full-screen phone/card composition repeatedly. A device UI should be one visual tool among many.
- Use transitions motivated by the story: match cut, whip pan, shape morph, wipe, parallax push, snap zoom, split-screen reveal, or a brief impact cut.
- Avoid constant zooming, random shaking, excessive glitch effects, and motion that competes with the narration.

### 3.3 Original character system

Create a small cast only when people improve the explanation. Every character must be original and visually distinguishable by silhouette, proportions, palette, clothing, and facial design.

For each recurring character, create:
- Name and narrative role.
- Age impression (do not infer or assert a real person's identity).
- Silhouette and body proportions.
- Face, hair, clothing, accessories, and signature prop.
- Primary and secondary colors.
- Emotional range: neutral, curious, confused, worried, shocked, determined, relieved, etc.
- Front, 3/4, side, and back design references (or matching SVG view components where practical).
- Expression sheet and at least three reusable poses.
- A concise consistency guide so the design does not drift between scenes.

**Optional recurring cyber-awareness cast**
Use these only when they suit the episode; do not force them into unrelated topics:
- **Rahi – Cyber Guide:** calm, capable guide; clean outfit in brand blue, blue accent, shield motif.
- **Ayan – Everyday User:** relatable user; expressive eyebrows and eyes; ordinary clothing; reacts naturally to events.
- **Shadow Caller – Threat Figure:** anonymous silhouette with restrained crimson rim light; never depict a real scammer or accuse a real person without verified evidence.

For a new topic, Claude may invent a completely new cast. Do not make every antagonist a hooded hacker; scams and threats can be represented through a deceptive message, fake interface, social-engineering voice, misleading link, or symbolic visual.

### 3.4 Copyright and asset rules

- Create original React SVG artwork, CSS shapes, procedural illustrations, and authored motion graphics.
- Do not copy a recognizable character, creator's signature style, copyrighted mascot, or trademarked brand identity.
- Do not use external image URLs or random stock photos as a substitute for original design.
- If the user provides a reference image, use it only for the requested high-level visual guidance; do not reproduce protected artwork exactly.
- Do not invent official app screens, police badges, bank logos, government seals, or brand marks. Use clearly fictional placeholder interfaces when exact reproduction is unnecessary.
- Keep all assets local to the project so the render does not depend on unstable remote URLs.

---

## 4. Color, Typography, and Layout System

Use the following as the default light blue-branded theme. For non-cyber topics, retain the same design discipline and light base, but tune the accent colours to the subject and explain the choice in the art-direction notes.

### 4.1 Default palette (light blue branding)

| Purpose | Color | Usage |
|---|---|---|
| Light background | `#EAF2FC` | Main canvas / bright airy negative space |
| Card surface | `#FFFFFF` | Information panels, UI surfaces, caption box fill |
| Card border | `#CBD9EE` | Subtle separation on light surfaces |
| Brand blue | `#2563EB` | Primary brand accent, caption box underline/edge, guidance, focus, links, progress |
| Blue tint | `rgba(37, 99, 235, 0.10)` | Soft blue fills, highlight panels, diagram backgrounds |
| Alert red | `#DC2626` | Danger, scam indicators, critical keywords |
| Alert tint | `rgba(220, 38, 38, 0.12)` | Red keyword badges / soft warning fills |
| Emerald | `#059669` | Safe action, success, resolution |
| Main text | `#0F1E3D` | Main captions and headlines (deep navy, dark on light) |
| Secondary text | `#51637F` | Supporting labels and metadata |

Red is an alert accent, not a color for every word. Highlight only the most meaningful warning terms. Use brand blue and emerald to communicate explanation and safety. On the light background, keep text navy or darker for contrast; never use light text without a solid surface behind it. Preserve accessible contrast in every combination.

### 4.2 Typography

- Bengali primary: **Hind Siliguri** (use installed/local font files when possible).
- Optional Bengali alternatives: **Noto Sans Bengali** or **Noto Serif Bengali**, depending on the visual direction and glyph quality.
- Numbers, codes, timestamps, short English technical labels: **JetBrains Mono**.
- Use a deliberate type scale with distinct roles. Do not render every word, headline, caption, and label at the same size.
- Use weight, size, color, spacing, and placement together to establish hierarchy. Size changes must communicate meaning—not be random decoration.
- Verify Bengali conjuncts, vowel marks, punctuation, and mixed Bengali/English lines in the actual render. Never assume that a font declaration alone guarantees correct shaping.
- Avoid long all-caps English phrases, tiny labels, decorative fonts for Bengali body text, and overly tight line spacing.

### 4.2.1 Mandatory Type Hierarchy for 1080×1920 Shorts

Use these as starting ranges, then adjust after checking a real phone-size preview. They are design roles, not inflexible pixel laws:

| Text role | Starting size | Weight | Purpose |
|---|---:|---|---|
| Hook / opening headline | 76–112 px | 700–800 | One strong question, claim, or short phrase |
| Main scene headline | 58–76 px | 700 | Names the current idea or reveal |
| Dominant number / key phrase | 84–128 px | 700–800 | A meaningful figure, amount, warning, or payoff |
| Subtitle / narration caption (inside its box) | 46–56 px | 600–700 | The primary attention anchor: the spoken words, boxed and eye-catching |
| Emphasized caption phrase in the box | About 1.08–1.15× caption size, or bold accent colour | 700–800 | Selective emphasis on one or two important words/phrases |
| Supporting explanation | 32–40 px | 500–600 | Short secondary context |
| Category tag / evidence label | 24–30 px | 600–700 | Brief metadata or scene category |
| Tiny UI detail | 18–22 px minimum | 500 | Only when essential; never use for key information |

**Hierarchy rules:**
- In every scene the primary text focus is the caption inside its caption box. Headlines, numbers, cards, and labels are secondary and must not visually outshine or crowd the caption box.
- Use size contrast intentionally within that rule: supporting headlines stay clearly smaller than or visually subordinate to the caption box presence; a key number may be bold, but never positioned or styled so it steals the eye from the boxed caption.
- A single visual card should normally contain one headline and no more than two or three short supporting lines. If more explanation is needed, split it into sequential beats instead of shrinking everything.
- Keep line height generous (usually around 1.2–1.4 for Bengali), with enough padding around text. Check conjuncts and vowel marks at actual output size.
- Do not enlarge every other word or animate each glyph independently. Use size changes for a meaningful word/phrase, not as a constant visual effect.
- Keep a consistent font family and role-based size across scenes. Scene-to-scene variation is welcome; arbitrary inconsistency is not.

### 4.2.2 Caption Box: Boxed, Attention-First, Selectively Emphasized

**Mandatory:** every narration caption is rendered inside a clearly visible caption box on every cue. The caption box is not decoration; it is the visual focal point of the scene, and the viewer's eye must land on it first. Never render a literal subtitle line floating on the background without its box.

**Caption box design (default):**
- Solid high-contrast surface such as `#FFFFFF` at roughly 0.92–1.0 opacity, with a subtle 1–2 px border in `#CBD9EE` plus a short accent edge or underline in brand blue `#2563EB` (red `#DC2626` border only over genuine danger cues, or emerald `#059669` over safe-action cues).
- Corner radius around 16–20 px, generous horizontal padding, and enough separation from characters, props, and headline layers so the box never merges with the scene; a soft blue-tinted drop shadow can lift the white box off a light background without looking heavy.
- Fixed, comfortable position near the lower third (inside the mobile safe area), consistent across the whole video so the eye learns where to look.
- Optional restrained entrance (short spring rise or a few frames of fade) that draws attention to the box without bouncing or flicker; the box stays fully steady while reading.

**Text inside the box:**
- Base caption: Hind Siliguri SemiBold (`600`) or Bold (`700`), normally 46–56 px for 1080×1920 output.
- Emphasis: Bold (`700`–`800`) for the one or two most important words/phrases in that cue—such as `OTP`, `UPI PIN`, `টাকা`, `ভুয়ো`, `চাপ দেবে না`, or a topic-specific reveal.
- Emphasis: Hind Siliguri Bold (`700`) for the one or two most important words/phrases in that cue—such as `OTP`, `UPI PIN`, `টাকা`, `ভুয়ো`, `চাপ দেবে না`, or a topic-specific reveal.
- Use the alert red `#DC2626` only for genuine danger/scam keywords; use brand blue `#2563EB` for explanation/focus and emerald `#059669` for safe actions. Do not color every emphasized word red.
- A highlighted phrase may be up to about 1.08–1.15× the base caption size, but keep it on the same baseline and preserve natural Bengali shaping. In many cues, bold/color alone is enough; do not enlarge it just because it is emphasized.
- Emphasize a complete phrase when changing only one word would distort the reading rhythm or Bengali grammar. Preserve punctuation and exact source wording.
- Keep the caption box background, padding, corner radius, accent treatment, and position consistent across cues so viewers can read captions without re-learning the layout. The boxed caption text can wrap to a maximum of two lines inside the box; the box height adapts to one or two lines without resizing the text.
- Do not resize the entire caption cue unpredictably to fit. Reflow into two balanced lines first; if it still cannot fit, reduce size slightly within the readability range and flag the cue if necessary.
- Never bold every word, color every word, or make every caption phrase jump/scale. Attention comes from the strong, consistent box plus selective emphasis, not from flashing or scaling text. Avoid karaoke-style word-by-word highlighting unless the user explicitly asks for it and the narration timing supports it.
- Caption emphasis must support the spoken meaning, not introduce new claims or change what the SRT says.
- The caption box is always the brightest, highest-contrast text container on screen. Scene headlines, number cards, and evidence panels must sit visually below it in contrast and pull; if a headline moment would pull the eye away from the boxed caption, subdue the headline layer for that beat.

**Captions and visual headlines keep separate jobs:** the boxed caption is the faithful narration track and the primary attention anchor; the larger headline is an editorial summary or visual hook in a separate layer. Do not put the headline inside the caption box, and do not let the two overlap or compete for the same eye position.

### 4.3 Mobile-safe composition

For 1080×1920 vertical video:
- Keep the most important information inside a central safe area; leave breathing room near top and bottom for platform UI.
- Keep the caption box away from the extreme bottom edge and inside the central safe area, so it reads instantly on a phone even with platform UI visible.
- Use no more than two boxed caption lines at a time unless the user specifically requests another format.
- Keep a clear distinction between the boxed narration caption (primary focus), visual headline (secondary), and tiny UI labels (tertiary).
- Do not let characters, props, or text overlap the caption box; reserve its screen region for the box in every scene's blocking.
- Check the result at actual phone-size preview, not only full-screen desktop.

---

## 5. Retention Design: First Frame to Final Frame

Retention is created by information progression, not by nonstop movement. Give viewers a reason to keep watching every few seconds.

### 5.1 Hook: first 0–3 seconds

- Start with the strongest question, risk, contradiction, surprising action, or outcome that is supported by the topic.
- Show the central conflict immediately. Do not begin with a logo animation, greeting, channel intro, or slow establishing shot.
- Use one memorable visual event: a number transforming, a message arriving, an object breaking, a map reveal, a sudden consequence, or a character reaction.
- Use a short kinetic headline, not a full sentence paragraph.
- The hook must be truthful and must pay off later in the video. No misleading threat or fabricated claim.

### 5.2 Middle: escalation and explanation

- Each beat must add at least one of: new information, consequence, proof, a visual demonstration, a character decision, a question, or a change in stakes.
- Aim for a meaningful visual change every 2–4 seconds and a larger composition/pattern break every 5–8 seconds, adapting to narration and topic complexity.
- A character's expression or action should respond to the story, not merely bob on screen.
- Use contrast: calm explanation → sharp reveal → brief visual pause → practical solution.
- Reveal information progressively. Do not show every answer in the first few seconds.
- Avoid repeated empty transitions, repetitive card pop-ups, and generic b-roll that does not prove or explain anything.

### 5.3 Ending: payoff and action

- Resolve the opening question or promise.
- Give one to three concrete takeaways, not a long checklist.
- End with the most relevant next action: a safe behaviour, a check to perform, an official reporting path, or a thoughtful CTA.
- For Indian cyber-financial-fraud episodes, a `1930` helpline / National Cyber Crime Reporting Portal reference may be included when relevant. Confirm current official details if browsing is available; do not insert `1930` into unrelated topics or imply it applies to every incident type.
- Hold the final key takeaway long enough to read. Do not cut off the last word, caption, audio tail, or CTA.
- Avoid a long generic “Like, Share, Subscribe” ending. A short, topic-relevant CTA is preferable.

### 5.4 Motion pacing rules

- No accidental static frame longer than about 2.5 seconds. Intentional dramatic holds are allowed when the silence or stillness has a clear purpose.
- Use `spring`, `interpolate`, and frame-based transforms with restrained easing.
- Keep camera motion subtle when captions are being read.
- Reserve impact shakes, glitch bursts, and fast zooms for moments that earn them.
- Give every important entrance and exit a readable animation state; avoid flicker and abrupt opacity changes.
- Keep motion coherent at 30fps; test fast movement for stutter and text readability.

---

### 5.5 Character Acting and Locomotion — Mandatory When Characters Are On Screen

A character design sheet is a **static reference**, not the finished animation. It is correct for a turnaround sheet to show front, side, and back poses standing still. In the final video, however, a character must perform story-motivated actions. Never place a static character PNG/SVG on screen for an entire scene and call it character animation.

**Non-negotiable rule:** whenever a character appears in a character-led scene, specify what the character is doing—not just how the character looks. A character must not remain in the same pose and position for a whole scene unless the stillness is a deliberate dramatic choice (for example, a brief shock pause, suspense beat, or emotional silence).

For every character appearance, plan the applicable details:
- `action`: a clear verb such as enters, walks, runs, turns, reaches, picks up, types, points, explains, recoils, steps back, raises a shield, hands over an object, or exits.
- `startPose` and `endPose`: the pose at the beginning and end of the beat.
- `screenPath`: where the character moves (for example, left-to-right, foreground-to-background, seated-to-standing, or stays planted while the upper body acts).
- `bodyMovement`: torso lean, weight shift, shoulder movement, crouch, rise, or twist.
- `headAndGaze`: head turn, tilt, nod, eye direction, and the specific object/person being watched.
- `faceActing`: timed changes to eyebrows, eyes, pupils, eyelids, and mouth; do not use one unchanged expression throughout.
- `armGesture` and `handAction`: point, wave, reach, grip, hold, tap, type, pull away, cover, or present an object as appropriate.
- `legAction`: walk/run cycle, step, pivot, crouch, recoil, or a deliberate stable stance.
- `propInteraction`: the exact contact or interaction with a phone, card, laptop, shield, document, door, or other story object.
- `startFrame`, `peakFrame`, and `endFrame`: when the movement begins, reaches its key pose, and settles.

**Timing and variety**
- For a character-led beat, introduce a meaningful action, pose, gaze, or expression change at least every 2–4 seconds, guided by narration. Do not add random movement just to satisfy a timer.
- A scene longer than about 2.5 seconds must not show a character frozen in one identical pose unless the storyboard labels the hold as intentional and explains its dramatic purpose.
- Avoid using a tiny vertical bob, breathing loop, or blinking as the only movement in a long scene. Idle animation is secondary texture, not the main action.
- Mix locomotion, gesture, interaction, acting, and reaction. Not every character needs to walk in every scene; a focused hand action or meaningful body turn can be more effective.
- Give actions anticipation, readable main movement, and a settle/reaction where appropriate. Avoid robotic instant pose swaps.
- Coordinate the character's gaze and hand with the prop. If the character taps a phone, the finger must reach the screen; if the character looks at a reveal, the eyes/head must turn toward it.
- Use stillness intentionally for a brief emotional beat, then resume action or cut to a new visual.

**Build a usable 2D character rig**
- Do not draw a character as one flat, indivisible SVG if the scene needs limb animation. Separate the SVG into independently transformable groups/layers: torso, head, hair, eyes, pupils, eyebrows, mouth, upper arms, forearms, hands, upper legs, lower legs, feet, clothing details, and held props as needed.
- Keep joint pivots near shoulders, elbows, wrists, hips, knees, and neck so limbs rotate naturally instead of sliding from their centres.
- Use frame-deterministic Remotion values (`useCurrentFrame`, `interpolate`, `spring`, and local frame offsets) for every movement. Do not rely on CSS keyframe loops, browser timers, or nondeterministic animation libraries for rendered motion.
- Create reusable action presets, but tailor their timing and pose to each scene. A reusable walk cycle must be interrupted or adjusted when the character stops, turns, reacts, or touches a prop.
- Use a simple character only when the visual direction genuinely calls for it. If a scene needs nuanced action that cannot be achieved with the current SVG rig, improve the rig or choose an animation approach that can deliver it; do not silently replace motion with a static image.

**Suggested reusable action library**
`enter`, `exit`, `walk`, `run`, `stop`, `turn_left`, `turn_right`, `look_up`, `look_down`, `look_at_phone`, `pick_up`, `put_down`, `type_on_phone`, `tap_screen`, `raise_phone`, `point_left`, `point_right`, `explain_open_palm`, `wave`, `reach`, `pull_hand_back`, `flinch`, `recoil_step`, `sit`, `stand_up`, `crouch`, `shield`, `relief_exhale`, and `celebrate`. Add topic-specific actions when needed. These are a vocabulary, not a fixed choreography template.

**Character-specific examples (adapt, do not force):**
- A guide character may enter the frame, walk beside a diagram, turn to camera, point to a danger marker, demonstrate a safe action, and exit.
- An everyday-user character may receive a message, look down at the phone, type, pause, notice a warning, recoil, put the phone down, and relax after understanding the safe step.
- A threat figure may emerge from behind a device, reach toward a fake interface, manipulate a misleading message, then fragment or retreat when the deception is exposed. Avoid repetitive generic “hacker typing” imagery.

### 5.6 Character Motion Acceptance Test

Before rendering the full video, inspect a short preview of every character-led scene. Confirm that:
1. The character changes pose or performs an intentional hold with a clear story reason.
2. The torso/head/arms/hands/legs that should move actually move independently.
3. Feet do not slide during a planted pose; hands do not miss the prop they touch.
4. Gaze and expression match the narration and event.
5. Movement has a clear start, readable action, and settle; no random jitter or constant idle bobbing.
6. Character movement and camera movement do not make captions difficult to read.

If an animated scene looks like a still illustration with only a pulsing scale, revise it before delivery.

---

## 6. Script, Storyboard, and Timeline Generation

Before coding, generate a compact production brief and a structured timeline. Do not immediately render a generic template.

### 6.1 Production brief

Create:
1. Topic and audience.
2. One-sentence promise.
3. Core question / curiosity gap.
4. Main emotional progression.
5. Verified facts and source notes (for factual subjects).
6. Art direction and chosen visual metaphor.
7. Character roster and consistency notes.
8. Palette and typography.
9. Intended duration, aspect ratio, and FPS.

### 6.2 Storyboard fields

For each scene or beat, create a data record with:
- `id`
- `startFrame` and `endFrame`
- `startMs` and `endMs` where source timestamps exist
- `retentionRole`: `hook`, `setup`, `curiosity`, `explanation`, `escalation`, `proof`, `reveal`, `prevention`, `payoff`, or `cta`
- `narrationText` (or exact source SRT text)
- `captionText` (exact SRT line when SRT exists)
- `visualDescription` (describe the actual designed composition, depth layers, lighting, and action—not just the subject)
- `shotType` and `cameraMovement`
- `activeCharacters` and `characterMood`
- `characterAction` (clear action verb for each visible character)
- `characterStartPose` and `characterEndPose`
- `characterPath` / `screenPath`
- `bodyMovement`, `headAndGaze`, `faceActing`, `armGesture`, `handAction`, and `legAction` as applicable
- `propInteraction` (what is touched, held, tapped, moved, or avoided)
- `actionStartFrame`, `actionPeakFrame`, and `actionEndFrame`
- `keyProps` / `UIElements`
- `onScreenText`
- `highlightKeywords`
- `motionStyle`
- `transitionIn` and `transitionOut`
- `sfx` and `musicCue`
- `factSource` / `factStatus` when factual claims appear

Choose scene lengths based on the sentence, idea, and visual action. A long subtitle cue can contain more than one visual sub-beat, but never alter the exact caption timestamps. A short cue should not be stretched only to fill a layout.

### 6.3 Example retention roles

| Role | Purpose | Example treatment |
|---|---|---|
| `hook` | Stop the scroll | Dramatic action + short question |
| `setup` | Establish context | Character and situation |
| `curiosity` | Create an open question | Partial reveal / unexplained clue |
| `explanation` | Make the mechanism clear | Diagram, animation, or UI simulation |
| `escalation` | Raise consequence | Visual chain reaction |
| `proof` | Support a claim | Source-backed number, evidence, or demonstration |
| `reveal` | Deliver the key insight | Visual transformation / reveal |
| `prevention` | Teach safer behaviour | Clear steps and positive visual language |
| `payoff` | Resolve the opening hook | Return to the opening visual with a new meaning |
| `cta` | Give the next action | One specific action / relevant reporting route |

---

## 7. Audio, SRT, and Frame-Accurate Synchronization

### 7.1 Measure audio

Use `ffprobe`:

```bash
ffprobe -v error -show_entries format=duration \
  -of default=noprint_wrappers=1:nokey=1 public/voiceover.mp3
```

Calculate:

```ts
const durationInFrames = Math.ceil(audioDurationSeconds * fps);
```

Use the exact measured duration for the composition. Do not assume every video is 60 or 66 seconds.

### 7.2 Parse SRT

Support standard SRT timestamp format:

```text
00:00:01,200 --> 00:00:03,450
বাংলা সাবটাইটেল এখানে
```

For each cue:
- Convert timestamps to milliseconds.
- `startFrame = Math.floor((startMs / 1000) * fps)`
- `endFrame = Math.min(durationInFrames, Math.ceil((endMs / 1000) * fps))`
- Preserve the exact cue text and cue order.
- Validate invalid timestamps, negative duration, overlaps, gaps, and cues beyond the audio duration.
- Do not force every cue to a minimum 15 frames if doing so would violate its real timestamp. Handle short cues with readable layout and transition design instead.

### 7.3 Caption display

- Use exact SRT text when the SRT is authoritative.
- Render every cue inside the styled caption box described in Section 4.2.2; no cue may appear as plain text floating on the video background.
- Preserve line breaks where useful, but reflow only for layout; do not paraphrase captions.
- Use a stable caption font size and weight inside the box across cues. Apply selective bold/colour emphasis to one or two meaning-bearing words or phrases; do not render every word bold by default.
- Follow the type hierarchy and caption-box rules in Sections 4.2.1 and 4.2.2. The boxed caption is the scene's primary attention anchor; keep other headlines, numbers, and panels visually subordinate so the viewer's eye goes to the caption box first.
- Do not enlarge individual words dramatically. Keep emphasized phrases on the same baseline, preserve Bengali glyph shaping, and use a modest 1.08–1.15× scale only when it improves comprehension.
- Choose emphasis based on meaning: threat/risk, key mechanism, important amount/number, turning point, or safety action. Do not highlight every technical term automatically.
- Preserve exact punctuation and source wording. If a keyword highlight is added, it must style the original text span and must not add, remove, or reorder words.
- If the cue is too long to read, do not silently alter its text or time. Reflow into balanced lines first; then use a small readable size adjustment within the recommended range or flag the timing issue.
- Keep caption entrance/exit subtle enough not to distract from reading: a short entrance for the box is welcome because it draws attention, but the box and text must then stay steady. Avoid per-word bouncing, random scaling, and excessive kinetic effects while viewers are reading.

### 7.4 Audio mix

- Voiceover is the priority and must remain intelligible.
- Keep background music below narration; automate ducking where practical.
- Use SFX only at meaningful beats. Avoid placing a loud impact over a key spoken word.
- Use only original, licensed, royalty-free, or user-supplied audio assets.
- Include the complete audio tail; do not abruptly truncate the last syllable.

---

## 8. Remotion Project Architecture

Use a maintainable React + TypeScript project. Keep content data separate from reusable components.

Suggested structure:

```text
bangla-explainer-remotion/
├── package.json
├── tsconfig.json
├── remotion.config.ts
├── public/
│   ├── voiceover.mp3              # optional supplied/generated narration
│   ├── music/                     # licensed / original music
│   ├── sfx/                       # licensed / original SFX
│   └── fonts/                     # locally available font files
├── src/
│   ├── index.ts
│   ├── Root.tsx
│   ├── MainComposition.tsx
│   ├── data/
│   │   ├── parseSrt.ts
│   │   ├── timeline.ts
│   │   └── projectConfig.ts
│   ├── styles/
│   │   ├── theme.ts
│   │   └── typography.ts
│   ├── components/
│   │   ├── CaptionTrack.tsx
│   │   ├── KineticHeadline.tsx
│   │   ├── ProgressIndicator.tsx
│   │   ├── InfoCard.tsx
│   │   ├── PhoneOrDeviceMockup.tsx
│   │   ├── EvidencePanel.tsx
│   │   ├── CharacterStage.tsx
│   │   ├── SoundTrack.tsx
│   │   └── Transition.tsx
│   ├── characters/
│   │   ├── CharacterOne.tsx
│   │   ├── CharacterTwo.tsx
│   │   └── AntagonistOrGuide.tsx
│   ├── scenes/
│   │   ├── HookScene.tsx
│   │   ├── ExplanationScene.tsx
│   │   ├── DemonstrationScene.tsx
│   │   ├── PreventionScene.tsx
│   │   └── EndCardScene.tsx
│   └── utils/
│       ├── animation.ts
│       ├── textHighlight.ts
│       └── formatTime.ts
└── out/
    └── final_video.mp4
```

Do not create unused boilerplate just to match this tree. Add or remove components to suit the topic.

### 8.1 Implementation rules

- Use Remotion APIs such as `useCurrentFrame`, `useVideoConfig`, `Sequence`, `interpolate`, `spring`, `staticFile`, `Audio`, and `Img` where appropriate.
- Prefer frame-deterministic animations. Do not rely on CSS animations or browser timers that may render inconsistently frame to frame.
- Avoid network-loaded assets during render. Use local project assets.
- Keep all timing values in frames or derive them from milliseconds using the configured FPS.
- Use reusable components, typed data, stable keys, and clean separation between scene data and visual rendering.
- Do not write one huge component containing the whole animation.
- Provide graceful fallbacks for missing optional audio, fonts, or visual assets.
- If a required dependency or command is unavailable, identify the exact blocker and provide the closest working deliverable; do not claim a render succeeded when it did not.

### 8.2 Suggested theme configuration

Keep design tokens in one file:

```ts
export const THEME = {
  colors: {
    background: "#EAF2FC",
    cardBg: "#FFFFFF",
    cardBorder: "#CBD9EE",
    brandBlue: "#2563EB",
    redAlert: "#DC2626",
    emerald: "#059669",
    text: "#0F1E3D",
    muted: "#51637F",
  },
  fonts: {
    bangla: "Hind Siliguri",
    mono: "JetBrains Mono",
  },
  fps: 30,
  width: 1080,
  height: 1920,
};
```

If the topic calls for another palette, change the tokens centrally rather than hardcoding inconsistent colors in individual components.

---

## 9. Required Visual Components

Build only the components the topic needs, but use a strong reusable system.

### 9.1 Character component

Each animated SVG character should support props such as:
- `mood`
- `pose`
- `action`
- `gesture`
- `facing`
- `screenX` / `screenY` or a parent transform
- `actionProgress` or frame-derived local timing
- `lookTarget` / gaze direction
- `isTalking` where mouth movement is useful
- `accentColor`

Create visually distinct emotions through eye shape, eyebrow angle, pupil direction, mouth shape, head tilt, shoulders, torso lean, and hand gesture. Avoid using a single static face for every scene. A character sheet may show a neutral standing pose; scene components must animate the character according to the timeline action.

### 9.2 Character rig, pose animation, and movement implementation

**A. Separate moving parts**

Use nested SVG `<g>` groups or equivalent layered elements. At minimum, separate the parts needed for the actions in the script:
- Root / world transform (position, scale, facing)
- Torso and clothing
- Neck and head
- Hair or accessories that can follow through
- Eyes, pupils, eyebrows, and mouth
- Left/right upper arms, forearms, and hands
- Left/right upper legs, lower legs, and feet
- Props (phone, laptop, card, shield, paper, etc.)

Set sensible transform origins / joint pivots. Keep the character's silhouette and proportions consistent across all poses. Do not use independent floating body parts that visually detach at joints.

**B. Animate from action data**

Store scene choreography as data rather than hard-coding one permanent pose. Example shape:

```ts
 type CharacterActionBeat = {
   characterId: string;
   action: string;
   startFrame: number;
   peakFrame: number;
   endFrame: number;
   fromPose: string;
   toPose: string;
   path?: { x: number; y: number }[];
   gaze?: string;
   mood?: string;
   propInteraction?: string;
 };
```

Derive local frame progress from `useCurrentFrame()` and animate the relevant SVG groups with `interpolate()` / `spring()`. Use key poses at anticipation, action peak, and settle. Avoid a single `scale()` animation being mistaken for full character animation.

**C. Build and reuse action presets**

Implement only the action presets needed by the episode, but make them genuinely different:
- Walk/run: alternating legs and counter-swinging arms, slight torso/head response, believable foot planting.
- Turn: rotate feet/hips/torso/head in a readable order rather than spinning the whole character flat.
- Reach/pick up: shoulder → elbow → wrist/hand motion; hand meets the object; object responds.
- Phone interaction: character looks at phone, raises or lowers it, taps/types, and reacts to the resulting screen state.
- Point/explain: shoulder and elbow articulate, hand/finger points to the intended screen location, gaze follows.
- Shock/recoil: quick anticipation, head/torso lean or step back, eyes/brows/mouth change, then settle.
- Relief: shoulders lower, facial tension releases, breathing/hand movement becomes calm.

**D. Animate objects and the environment too**

When story-relevant, animate props independently: a notification arrives, phone vibrates, button depresses, message types in, link expands, payment request flips into a warning, shield blocks an incoming threat, diagram nodes connect, or evidence pins attach to a board. Synchronize these events with the character's gaze and gestures.

**E. Compose movement in layers**

Character motion, prop motion, background/parallax motion, and camera motion should be separate systems. Do not move every layer in the same direction at the same speed. Use depth and camera motion to support action, not to hide a static character. Keep the screen composition and caption safe area in mind throughout.

**F. No fake motion**

The following do not count as sufficient character animation for a character-led scene: one static full-body SVG with only scale pulsing, repeated up/down bobbing, blinking alone, repeated identical hand-wave loops, or sliding a flat character PNG across the screen. These may be used as minor secondary motion, never as the entire acting performance.

### 9.2 Visual information card

- Use a short headline and only essential supporting text.
- Use a single dominant number or phrase where possible.
- Highlight topic-critical warning terms in red for cyber-safety scenes; do not make every word red.
- Animate in with a restrained spring or slide and maintain enough screen time to read.
- Keep card styling consistent without repeating the exact same layout in every scene.

### 9.3 Progress indicator

A subtle progress line can use the blue-branded gradient `#DC2626 → #2563EB → #059669`. It must not become a distracting decoration or imply a countdown unless the story actually has one.

### 9.4 Device / UI simulation

- Create fictional but believable interface elements where needed.
- Animate touch, typing, message arrival, link opening, request/approval, error state, and system response.
- Show only UI details that serve the narration.
- Do not depict a dangerous action as safe. When demonstrating a scam, make the deceptive or unsafe nature clear.

### 9.5 Final action card

The ending should include a clear, relevant action. For cyber-financial fraud in India, use official reporting guidance only after verifying the current wording and route when possible. Keep the callout large, calm, and readable.

---

## 10. Rendering and Quality Assurance

### 10.1 Render defaults

Default output:
- Resolution: `1080×1920`
- Aspect ratio: `9:16`
- FPS: `30`
- Codec: H.264
- Quality: CRF around `18` (adjust if render environment requires)
- Output: `out/final_video.mp4`

Example:

```bash
npx remotion render src/index.ts MainComposition out/final_video.mp4 \
  --codec=h264 --crf=18
```

Read the project's current Remotion CLI help if the installed version uses different command options. Do not assume an outdated CLI syntax.

### 10.2 Automated checks

Before delivery:
1. Confirm the output file exists and is non-zero size.
2. Read final video metadata with `ffprobe`.
3. Confirm resolution, FPS, duration, codec, and audio stream presence.
4. Compare final duration against the master narration duration; explain any unavoidable frame-rounding difference.
5. Confirm no scene exceeds the composition duration.
6. Confirm every supplied SRT cue is represented at its exact frame interval (within frame rounding).
7. Check that the final caption and audio tail are not cut off.
8. Check that all assets are local and no broken/missing images appear.

### 10.3 Visual checks

Render contact sheets or representative frames from:
- First 0–3 seconds.
- Every major scene transition.
- Character close-ups and expression changes.
- Any dense typography or infographic scene.
- Final 3–5 seconds.

Inspect for:
- Bengali glyph shaping and conjuncts.
- Correct spelling and punctuation.
- Text clipping, overlap, poor contrast, and tiny labels.
- Consistent character design and colors.
- Repetitive compositions or dead static stretches.
- Motion blur / effects that reduce legibility.
- Safe margins for phone viewing.

If a problem is found, fix and re-render. Do not deliver a known-broken render as final.

---

## 11. Deliverables

When the environment supports file creation and rendering, provide:
1. `final_video.mp4` — final rendered video.
2. `SKILL.md` is the production guide; do not overwrite it when generating an episode.
3. `storyboard.md` — scene-by-scene visual plan.
4. `timeline.ts` or `timeline.json` — frame-based scene/caption data.
5. `character-design-sheet.png` — original character reference sheet where characters are used.
6. Project source folder or ZIP — Remotion code and local assets.
7. `qa-report.md` — duration, resolution, FPS, audio/SRT sync status, and any limitations.

Do not claim to have delivered items that were not actually created. If rendering is blocked, provide the completed source project and state exactly what remains.

---

## 12. Autonomous Decision Rules

When a detail is unspecified, make the best creative decision and continue. Do not interrupt the user with a long questionnaire.

Use these defaults:
- Platform omitted → YouTube Shorts.
- Aspect ratio omitted → 9:16.
- Resolution omitted → 1080×1920.
- FPS omitted → 30.
- Topic only → 45–60 second concise explainer.
- Language omitted → natural Indian Bengali for this project.
- Visual style omitted → cinematic 2D / 2.5D hybrid with original characters and editorial motion graphics.
- Palette omitted → default light blue-branded palette for all topics; choose and document a fitting accent variation for non-cyber topics.
- Characters omitted → invent only the minimum cast needed.
- Music omitted → subtle licensed/original instrumental bed if available; otherwise render without music rather than using unlicensed tracks.

Ask one concise question only when a missing input genuinely prevents a meaningful final result—for example, a required user voiceover that must be synchronized exactly but is not supplied, or a required brand/logo asset that cannot be inferred.

Do not ask for approval after every production stage. Make sensible decisions, build, inspect, and improve the result.

---

## 13. Topic Invocation Examples

The user should be able to start an episode with a short message. Interpret it as a full production request.

**Example A — topic only**

```text
Topic: QR Code Scam in India
Create a 50–60 second Bangla animated explainer. Research the key safety facts, write the narration, invent original characters, storyboard every beat, build the Remotion project, and render the final 9:16 video.
```

**Example B — audio and SRT supplied**

```text
Use the uploaded voiceover.mp3 and subtitles.srt as the master sources. Create a fresh visual concept and original characters for this topic. Preserve the narration and SRT wording exactly, synchronize every scene and caption, and render the finished Short.
```

**Example C — script supplied**

```text
Use my script as the content source. Create an original high-retention Bangla animation, with a scene-by-scene storyboard, character design, motion graphics, typography, and sound plan. Do not invent facts or change the script's meaning.
```

---

## 14. Final Acceptance Checklist

A video is complete only when the applicable items below are satisfied:

- [ ] The hook starts immediately and pays off later.
- [ ] The video has a clear beginning, escalation, explanation, and ending.
- [ ] Every scene adds information, emotion, proof, or a meaningful visual change.
- [ ] Scene layouts, shot sizes, and transitions have intentional variation.
- [ ] Characters are original, expressive, and consistent.
- [ ] Character-led scenes contain story-motivated full-body / limb / facial acting, not just a static standing pose or scale pulse.
- [ ] Character actions, gaze, hands, props, and scene blocking match the narration.
- [ ] Any intentional static hold is brief and has a clear dramatic reason.
- [ ] Every narration caption is rendered inside a clearly styled caption box, and the caption box is the scene's primary attention anchor (headlines and cards do not outshine it).
- [ ] Typography has a clear role-based hierarchy; the boxed caption, headlines, dominant numbers, supporting copy, and labels have distinct roles and sizes.
- [ ] Caption box text uses a stable readable base size with selective bold/colour emphasis—not all-bold or random word scaling, and never plain unboxed text.
- [ ] Emphasis is limited to the most meaningful one or two words/phrases per cue and does not alter the source caption.
- [ ] Bengali glyphs, conjuncts, vowel marks, and mixed-language text render correctly on a phone-size preview.
- [ ] Colors communicate hierarchy and are used consistently.
- [ ] On-screen words are concise and correctly spelled.
- [ ] Voiceover remains clear above music and SFX.
- [ ] SRT captions are exact and frame-synchronized when an SRT is provided.
- [ ] Final duration and technical metadata have been checked.
- [ ] Final action / CTA is useful and relevant to the topic.
- [ ] No unlicensed music, copied character, fake evidence, or unsupported claim is present.
- [ ] Output files and any limitations are reported honestly.

**The final standard:** It should feel like a carefully directed animated mini-documentary—not a slideshow with moving text or static characters pasted onto a background. Characters should act, react, move through the scene, and interact with the visual story whenever the narration calls for it.
