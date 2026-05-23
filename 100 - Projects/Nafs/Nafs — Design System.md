# 🎨 Nafs — Design System

Parent: [[Nafs]]

---

## Color Palette
- Background: #0C0C10
- Surface: #1A1A1E
- Card: #141418
- Gold accent: var(--gold)
- Text primary: var(--tx)
- Muted: var(--mt)

## CSS Custom Properties
- var(--mt) — muted text
- var(--tx) — primary text
- var(--gold) — gold accent (selected states, premium, highlights)

---

## Typography
- Mobile-first, 360px base width
- Clean, minimal — no decorative fonts
- Premium feel — generous spacing

---

## Component Style
- Chip-based inputs (not sliders, not emoji, not rings)
- Cards with subtle borders
- Dark surfaces — never white or light backgrounds
- Gold used sparingly — only for selected/active/premium states

---

## Screens
- Today (ReflectScreen) — daily logging + Friday-aware UI
- Reflections (ProgressScreen) — history, signals, heatmap
- Settings

---

## Friday UI (Phase 2F)
- Special Friday card on Today screen
- Dhuhr prayer labeled as Jumu'ah
- Qur'anic ayah 62:9 displayed on Fridays
- isFriday computed from local device date
- Religious text exact — never paraphrased

---

## Aesthetic Direction
- Dark, premium, intentional
- Feels like a serious tool not a toy
- No streaks UI, no scoring rings, no gamification visuals
- Calm — never urgent or pushy