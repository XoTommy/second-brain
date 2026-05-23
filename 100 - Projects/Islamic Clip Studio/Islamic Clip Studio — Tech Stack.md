# ⚙️ Islamic Clip Studio — Tech Stack

Parent: [[Islamic Clip Studio]]

---

## Frontend
- Next.js
- UI theme: dark warm charcoal #0B0E0D
- Islamic green accent: #38AC72
- Gold accent: #C29438
- Font: DM Sans

## Backend
- FastAPI (Python)
- yt-dlp: YouTube download
- AssemblyAI: transcription (Arabic + English)
- Groq / llama-3.3-70b: clip selection AI
- FFmpeg: video cutting + subtitle burning

## Infrastructure
- Cloudflare R2: file storage
- Railway: backend hosting
- Stripe: payments

---

## V1 Architecture (Command Line)
- Built as Python script first
- yt-dlp + AssemblyAI + Groq + FFmpeg pipeline
- Reached working clip generation state
- Subtitle rendering is the outstanding issue

---

## Outstanding Issue
Subtitle rendering quality needs fix before launch.
Subtitles generate but rendering into video needs improvement.
This is the only blocker between V1 and soft launch.

---

## 4 UI Screens Built
1. Dashboard
2. Upload
3. Processing
4. Results