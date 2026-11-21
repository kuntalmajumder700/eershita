# Documentary Skill — ব্যবহারের নির্দেশিকা (INSTRUCTIONS)

এই ফাইলটা পড়ে তুমি নিজেই স্কিলটা Claude-এ বসাতে পারবে আর প্রথম ভিডিও বানাতে পারবে।

---

## ধাপ ১: ফাইল ডাউনলোড

সবচেয়ে সহজ — পুরো repo ZIP:
👉 [ZIP ডাউনলোড](https://github.com/kuntalmajumder700/eershita/archive/refs/heads/main.zip)

ZIP খুললে পাবে:

```
documentary-longform-video/
├── SKILL.md                ← মেইন স্কিল ফাইল
└── references/
    ├── style_guide.md      ← ভিজ্যুয়াল স্টাইল (কালার, ফন্ট, মোশন)
    └── templates.md        ← সব ধাপের টেমপ্লেট
```

⚠️ ফোল্ডারের নাম ঠিক রাখো: `documentary-longform-video`

## ধাপ ২: Claude-এ ইনস্টল

**Claude.ai ( ওয়েব ):**
1. Settings → **Capabilities** → **Skills**
2. `documentary-longform-video` ফোল্ডারটা ZIP করো (ফোল্ডারের ভেতরের ৩টা ফাইলসহ)
3. ZIP-টা আপলোড করো → স্কিলের পাশে ✓ enable দেখালেই রেডি

**Claude Code (টার্মিনাল):**
```bash
git clone https://github.com/kuntalmajumder700/eershita.git
mkdir -p ~/.claude/skills
cp -r eershita/documentary-longform-video ~/.claude/skills/
```

## ধাপ ৩: প্রথম ভিডিও শুরু

নতুন Claude চ্যাটে শুধু লেখো:
```
start a documentary video
```

তারপর Stage 1-এ Claude তোমাকে ৫টা প্রশ্ন করবে:
1. **টপিক** — কী নিয়ে ভিডিও (সাথে সবচেয়ে ড্রামাটিক ফ্যাক্টটা বললে ভালো)
2. **দৈর্ঘ্য** — short 8-12 min / standard 15-20 min / deep dive 25-30 min
3. **ভাষা** — English / Hindi / Hinglish / Bangla
4. **থাম্বনেইল** — চাই কি না (ডিফল্ট: হ্যাঁ)
5. **অডিও** — "I will send MP3/WAV" নাকি "generate timing without audio"

প্রতিটা ধাপে Claude একটা **RUN CARD** দেখাবে — টপিক, টার্গেট রানটাইম, কতদূর এগোল, চ্যাপ্টার লিস্ট। ওটায় সবসময় নজর রাখো।

## ধাপ ৪: স্টেজগুলো কী ঘটবে

| Stage | Claude কী করবে | তোমার কাজ |
|---|---|---|
| 1. Brief | প্রশ্ন + চ্যাপ্টার স্পাইন + RUN CARD | উত্তর দাও, approve করো |
| 2. Research | সাইটেশনসহ রিসার্চ ব্রিফ (ফাইলে) | পড়ে ভালো লাগলে "continue" |
| 3. Script | নারেশন বিটস + **Typography Plan** (কোন বড় কার্ড কত সেকেন্ডে আসবে) | এডিট/approve; ভয়েসওভার রেকর্ড করবে নাকি ছাড়াই চলবে বলো |
| 4. Timing | SRT/MP3/WAV থাকলে সেটাই truth; না থাকলে নিজেই Timing Sheet বানাবে | শুধু রেজাল্ট দেখে "continue" |
| 5. Scene plan | শট লিস্ট + asset checklist | স্ক্রিনশট/ছবি দাও, **বা শুধু বলো "use fallbacks"** |
| 6. Render | এক চ্যাপ্টার করে ভিডিও/Remotion প্রজেক্ট | পরিবর্তন বলো — শুধু ওই চ্যাপ্টারে ধরা হবে |

## অডিও নিয়ে ৩টা পথ (কোনোটাতেই আটকাবে না)

- **A.** MP3/WAV + SRT দিলে → SRT-ই টাইমিং সত্য, সব ওর উপর সিঙ্ক
- **B.** শুধু MP3/WAV → Whisper/CapCut দিয়ে SRT বানিয়ে দাও; Claude ততক্ষণ অনুমানে এগোবে
- **C.** কিছু না দিলে → script ÷ WPM দিয়ে টাইমিং হবে; চাইলে Claude TTS-ও করবে। ভিডিও সাইলেন্স/মিউজিক দিয়ে হবে, পরে তোমার অডিও ঢুকিয়ে দিলে রিটাইমিং লাগবে না

ভয়েসওভার ফাইলের নাম: `part1.mp3`, `part2.mp3`, ... (প্রতি চ্যাপ্টারে একটা); SRT হলে একই নামে।

## অ্যাসেট দেওয়ার নিয়ম

- নাম: `scene07_guardian.png` — যে শটে লাগবে সেই নম্বর
- কাঙ্ক্ষিত: নিউজ স্ক্রিনশট, আর্কাইভ ফটো, সত্যিকারের মানুষের ছবি (কখনো AI-বানানো মুখ না), লোগো, ছোট B-roll, মিউজিক
- না দিলে: সব ফলব্যাকে চলবে — অ্যানিমেটেড টেক্সট ক্লিপিং, ম্যাপ, ডায়াগ্রাম। **"use fallbacks"** লিখলেই হবে

## শেষ ধাপে

- প্রতি চ্যাপ্টারের ভিডিও/প্রজেক্ট + শট লিস্ট + কোন শট জেনারেটেড/প্লেসহোল্ডার
- সব শেষে থাম্বনেইল: ৩-৫ শব্দের বড় টাইটেল + ড্রামাটিক ভিজ্যুয়াল
- ফাইনাল **Quality gate** checklist মিলিয়ে নাও

## ঝামেলা হলে

- স্কিল ট্রিগার না হলে: চ্যাটে লেখো `documentary-longform-video skill use kore start a documentary video`
- বড় কার্ড কম লাগছে মনে হলে: বলো "check the 40-60 second rule"
- রেন্ডার সম্ভব না হলে Claude নিজেই Remotion (React) প্রজেক্ট দেবে — `npm install` → `npx remotion render` দিয়ে চালাবে
