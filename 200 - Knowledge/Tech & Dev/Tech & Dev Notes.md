# ⚙️ Tech & Dev Notes

---

## My Stack By Project

| Project | Frontend | Backend | Storage | Hosting |
|---|---|---|---|---|
| Nafs | React 18 + Vite | None | localStorage | Netlify/Vercel |
| IDCard Studio | React | Firebase | Firestore + Storage | Firebase |
| Islamic Clip Studio | Next.js | FastAPI | Cloudflare R2 | Railway |
| BuildCalc | Static HTML/JS | None | None | Netlify |
| Sim Racing Controller | Flutter | Python | None | Local PC |
| Sabr Walls | Flutter | None | None | App Stores |
| True Form | Flutter | TBD | TBD | App Stores |

---

## AI-Assisted Development Rules
- Always approve plan before any code is written
- Surgical patches only — never rewrite whole files
- Additive changes only — zero regression risk
- Self-audit table on every patch
- Test checklist before marking done

---

## Firebase Notes
- Auth: never store passwords in Firestore
- Security Rules are non-negotiable — always implement
- Firestore structure: keep flat where possible
- Storage: Firebase Storage for photos/files

---

## Flutter Notes
- Android first — broader reach, easier launch
- iOS second after Android stable
- 360px base width for mobile UI
- sensors_plus package for gyroscope

---

## React Notes
- Vite for fast builds
- localStorage for simple persistence
- CSS custom properties for theming
- Mobile-first 360px width

---

## Python Notes
- FastAPI for REST APIs
- WebSocket for real-time (Sim Racing Controller)
- vJoy + ViGEm for virtual controller simulation
- yt-dlp for YouTube downloading
- FFmpeg for video processing
- AssemblyAI for transcription

---

## General Dev Principles
- Build the simplest version that works first
- Add complexity only when needed
- Never over-engineer an MVP
- Real users reveal real problems — ship and learn