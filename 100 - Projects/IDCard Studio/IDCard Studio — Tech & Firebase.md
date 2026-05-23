# ⚙️ IDCard Studio — Tech & Firebase

Parent: [[IDCard Studio]]

---

## Stack
- Frontend: React
- Backend: Firebase
- Auth: Firebase Authentication
- Database: Firestore
- Storage: Firebase Storage (photos)
- Hosting: Firebase Hosting or Netlify

---

## Firebase Setup — Phase 1 (Next Step)
- Firebase Authentication setup
- Firestore database setup
- Security Rules implementation
- School role vs Admin role separation in rules

---

## Security Rules — Core MVP Requirement
- Schools can only read/write their own students
- Admin can read/write everything
- No cross-school data visibility for school role
- Passwords NOT stored in Firestore — Firebase Auth handles this

---

## Firestore Data Structure

schools collection:
- schoolId → name, enabled, createdAt

students collection:
- studentId → schoolId, name, class, section, photoURL, status, createdAt

---

## Export Logic
- Admin filters students by school / class / section / status
- Single export button exports current filtered view only
- Excel: student data rows
- ZIP: corresponding student photos

---

## MVP Rules
- Passwords never in Firestore
- Security rules are not optional — core requirement
- Build speed is top priority
- No feature creep beyond defined scope