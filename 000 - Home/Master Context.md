# 🧠 Master Context — Amen's Second Brain

## Who I Am
- Solo builder and entrepreneur, Kozhikode, Kerala, India
- No formal coding background — AI-assisted development
- Building a tech ecosystem for the global Muslim community and beyond
- Goal: meaningful recurring income through products I believe in
- GitHub: XoTommy | Obsidian second brain synced to github.com/XoTommy/second-brain

---

## Builder Rules (Apply To All Projects)
- Approve plan before any code
- Surgical file-scoped patches only — never rewrite whole files
- Additive changes only — zero regression risk
- Self-audit table + test checklist on every patch
- Speed over perfection in early stages
- One primary project at a time

---

## 🌙 NAFS
Islamic muhasabah app — NOT a habit tracker, NOT a streak app
Platform: React 18 + Vite, localStorage, targeting Google Play + App Store
Width: 360px mobile-first
Storage: nafs-state-v2

### Design System
- Background: #0C0C10 | Surface: #1A1A1E | Card: #141418
- Gold accent: var(--gold) | Text: var(--tx) | Muted: var(--mt)
- CSS custom properties throughout
- Chip-based inputs — no sliders, no emoji, no rings

### Completed Phases
- Phase 1: Removed streak card/scoring UI, removed unverified hadith, renamed Progress → Reflections
- Phase 2A: Upgraded to nafs-state-v2 — four nullable 1–5 signals (mood, energy, discipline, distraction), structured premium object, safe migration in loadState(), consolidated storage.js
- Phase 2B: Signal capture UI in ReflectScreen — chip-based, toggle/deselect, optional/skippable, gold for selected, single handleSignal(field, value) handler
- Phase 2C: Signal display in Reflections — read-only, between .reflection-summary and .reflection-note-block, SIGNAL_LABELS constant, null-safe IIFE, "discipline" renders as "Intention"
- Phase 2F: Friday-aware Today screen — special Friday card, Dhuhr labeled Jumu'ah, Qur'anic ayah 62:9 on Fridays, isFriday from local device date

### Current Status
Phase 2 complete — incremental polish ongoing
Next: Phase 3 — Intelligence Engine (premium hero feature)

### Intelligence Engine (Phase 3 — Upcoming)
Weekly AI insight report — reads signals, worship logs, patterns
Calm, private, emotionally intelligent output
Premium only — hero feature that justifies subscription

### Monetization
- Free: daily logging, signals, heatmap, reflections, Friday UI
- Premium subscription: Intelligence Engine, monthly summaries, PDF export
- One-time: themes, PDF export
- Regional pricing: Tier 1 full, Tier 2 ~50%, Tier 3 ~25%
- Launch: timed lifetime access offer

### Dev Rules (Nafs-Specific)
- Religious text NEVER paraphrased — exact wording only
- Storage schema changes need explicit approval
- NZT-mode for deep pre-implementation analysis
- Named skills: nafs-code-builder, nafs-mobile-ux, nafs-brand-identity, nafs-emotional-design, nafs-copy-editor, nafs-qa-tester

### Growth
- Muslim micro-creator outreach (primary)
- Reddit: r/islam, r/productivemuslim
- Telegram + WhatsApp Islamic groups
- Ramadan campaign — biggest acquisition moment
- ProductHunt launch

---

## 🪪 IDCARD STUDIO
Private React + Firebase web app for family ID card printing business
Status: UI complete — Firebase Phase 1 setup is next step
Priority: HIGH — real orders waiting

### Two Roles
- School: add/edit/delete students, upload photos, cannot export
- Admin: create schools, view/filter all students, export Excel + photo ZIP, enable/disable schools

### MVP Rules
- Passwords NEVER in Firestore — Firebase Auth handles this
- Security Rules are non-negotiable core requirement
- School dashboard: instruction + Add Student + simple table only (Photo/Name/Class/Section/Status/Actions)
- Single "Export Current List" button — exports active filters only
- Duplicate entries: warn but don't block
- Missing recommended fields: show "Needs details" badge
- NO charts, analytics, bulk select, credential viewing in MVP
- Build speed is top priority

### Stack
React + Firebase Auth + Firestore + Firebase Storage
Theme: white + deep navy #1B2E5E

---

## 🧱 BUILDCALC
Live at: buildcalc-tools.netlify.app
Free static home materials calculator site
Status: Live — grow organically
Priority: Medium — passive income

### Current Calculators
Concrete slab, footing, gravel, mulch, brick/block

### Add Next
Paint, tile, fence, flooring, roof, deck, drywall

### Monetization
Google AdSense + Amazon affiliate links + $0.99 PDF report via Stripe

### Growth
SEO (primary) + Reddit r/DIY r/HomeImprovement + Google Search Console

### SEO Done
sitemap.xml, robots.txt, og:image, FAQ schema

---

## 🎬 ISLAMIC CLIP STUDIO
AI SaaS — converts Islamic lectures/khutbahs/podcasts into viral short clips
Status: V1 built — subtitle rendering is the only blocker for soft launch
Priority: Medium

### Stack
Next.js + FastAPI + yt-dlp + AssemblyAI + Groq/llama-3.3-70b + FFmpeg + Cloudflare R2 + Railway + Stripe

### UI Theme
Dark warm charcoal #0B0E0D + Islamic green #38AC72 + gold #C29438 + DM Sans
4 screens: Dashboard, Upload, Processing, Results

### Differentiator
Win by Islamic specificity — not competing feature-for-feature with Opus Clip
Better AI prompts for Islamic moments, Arabic+English subtitle accuracy, Muslim creator trust

### Pricing
Free (3 clips) | Creator $19/mo | Studio $49/mo | Agency $129/mo

### Target
Islamic YouTube channels, mosque media teams, dawah orgs, Muslim podcast producers

---

## 🎮 SIM RACING CONTROLLER
Mobile app — turns phone into sim racing controller for PC over WiFi
Status: Planning — builds after Nafs + IDCard Studio
Stack: Flutter (mobile) + Python PC companion app

### 3 Presets
1. Standard Xbox layout — ViGEm XInput
2. Racing preset — Xbox + gyroscope tilt steering — ViGEm
3. Sim Rig (hero) — touchable steering wheel graphic + auto-return to neutral + two sliding pressure pedals (throttle/brake, slide up = more pressure) — vJoy DirectInput
Games detect as real sim wheel: Forza Horizon 5, Assetto Corsa, BeamNG

### Monetization
- Free: all presets, 30 min sessions, rewarded ad for +30 min
- Premium: $4.99/mo or $29.99/year — unlimited, customization
- Launch lifetime: $49.99 — 3 weeks only, gone forever

### Marketing
Pure short-form video — screen record real gameplay — self-demonstrating product
TikTok + Reels + Shorts + Reddit r/simracing r/ForzaHorizon r/BeamNG

---

## 🕌 SABR WALLS
Minimal Islamic wallpaper app
Status: Planning — low effort, high passive potential
Platform: Flutter — Android first

### Colors
Deep Black #0B0B0B | Soft White #F5F5F5 | Gold #C8A951 | Dark Blue #0D1B2A

### Monetization
Free core collection + Premium $1.99/mo or $9.99/year + themed packs $0.99–$2.99

### Growth
Pinterest (primary — pin every wallpaper) + Instagram + Reddit

---

## 💪 TRUE FORM
Premium men's self-improvement app
Status: Planning — builds after Nafs, BuildCalc, Sim Racing Controller
Platform: Flutter — Android first

### Tagline
"Your potential score? Unwritten. We'll build the road. You decide how far you go."

### 5 Pillars
Facial Aesthetics | Body & Fitness | Grooming & Style | Personality & Mindset | Lifestyle & Discipline

### Hero Feature — Honest Rating System
- Free: photo upload → tier rating (Raw / Developing / Refined / Elite)
- Paid ($2.99 unlock): honest number rating e.g. 5.8/10 with specific breakdown
- No ceiling on potential ever implied — honest without being cruel

### Monthly Community Plan
All free users get same structured plan simultaneously — rotates monthly
Creates shared experience + retention without manipulation

### Monetization
Free tier + $2.99 rating unlock + $9.99 single program + $4.99 content library
Subscription: $12.99/mo or $79.99/year
Regional: Tier 1 full | Tier 2 ~$6.99 | Tier 3 ~$2.99

---

## 🕌 DUA REMINDER APP (Early Planning)
Flutter, minimal/distraction-free, authentic hadith only, no gamification
Forest green + warm cream UI
21 duas: Morning / Evening / Sleep categories

---

## 📱 SABR WALLS (see above)

---

## 🧭 Build Order
1. Nafs — complete phases, launch ← ACTIVE
2. IDCard Studio — MVP live ← ACTIVE
3. BuildCalc — grow organically ← LIVE
4. Islamic Clip Studio — fix subtitles, soft launch
5. Sim Racing Controller
6. Sabr Walls
7. True Form (biggest, last)

---

## 💰 Monetization Philosophy
- Free tier must be genuinely useful — never crippled
- Premium adds depth, not basics
- Regional pricing captures global markets
- Launch lifetime offer: timed, never returns
- No ads in Islamic products — ever
- Recurring revenue over one-time always

---

## 🌍 Islamic Content Rules
- Religious text NEVER paraphrased — exact wording only
- Hadith must be verified — if unverifiable, don't use it
- No unverified quotes attributed to Islam
- One wrong religious text = trust destroyed forever

---

## 📈 Growth Philosophy
- Muslim audience: cluster-based, trust-driven
- Creator outreach > algorithmic channels
- Ramadan = peak Islamic app moment every year
- Self-demonstrating products: show don't tell
- Pinterest for visual products, short-form video for demo products
- SEO for utility tools