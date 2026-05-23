# 📋 IDCard Studio — MVP Rules

Parent: [[IDCard Studio]]

---

## Non-Negotiable Rules

### Data & Security
- Passwords NEVER stored in Firestore — Firebase Auth handles all of this
- Firebase Security Rules are a core MVP requirement — not optional
- Schools can only see their own students — never cross-school data
- Admin has full visibility — schools have zero visibility of each other

### Export
- Single "Export Current List" button only
- Export always reflects active filters — no separate export flows
- Two formats: Excel (student data) + ZIP (photos)

### School Dashboard
- Shows: instruction text, Add Student button, simple table only
- Table columns: Photo / Name / Class / Section / Status / Actions
- Nothing else — no analytics, no charts, no extra UI

### Student Entries
- Duplicate entries: warn but DO NOT block
- Missing recommended fields: show "Needs details" badge
- Do not prevent submission for missing optional fields

### What Is Banned From MVP
- ❌ Charts or analytics
- ❌ Bulk select
- ❌ Admin viewing school credentials
- ❌ Multiple export buttons
- ❌ Any feature not listed in scope

### Speed Rule
Build speed is the top priority.
Real orders are waiting.
Do not over-engineer. Ship clean and fast.