# ⚙️ Nafs — Tech Stack

Parent: [[Nafs]]

---

## Core
- **Framework:** React 18 + Vite
- **Target:** Google Play + App Store (mobile web app)
- **Storage:** localStorage — nafs-state-v2
- **Width:** 360px mobile-first

---

## Storage Schema (nafs-state-v2)
- Four nullable 1–5 signals: mood, energy, discipline, distraction
- Structured premium object
- Safe migration logic in loadState()
- Consolidated in storage.js
- schemaVersion tracked — migrations are explicit and approved

---

## Key Files
- `storage.js` — all localStorage logic lives here
- `ReflectScreen` — daily logging + signal capture UI
- `ProgressScreen` (renamed: Reflections) — signal display + history

---

## Dev Rules
- Surgical file-scoped patches only
- Never touch storage schema without explicit approval
- Additive-only changes — zero regression risk
- Self-audit table + test checklist on every patch

---

## Signals System
- mood, energy, discipline, distraction
- All optional — skippable
- Chip-based UI, toggle/deselect
- Gold accent for selected state
- "discipline" renders as "Intention" in display
- Single handleSignal(field, value) handler

---

## NZT Mode
Deep pre-implementation analysis before any code is written.
Plan approved by Amen first, then surgical patch delivered.