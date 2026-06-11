# Product Roadmap — TutorLink

**Last updated:** June 11, 2026
**North-star metric:** Weekly completed lessons (video call ≥ 10 min on a confirmed booking)

---

## Sprint 1 — Shipped (April 23 – May 13, 2026)

| Story | Status |
|---|---|
| Supabase auth + route protection | ✅ Done |
| Tutor and student registration with role-specific fields | ✅ Done |
| Booking flow: search → slot → confirm | ✅ Done |
| Dashboard navigation | ✅ Done |
| Bilingual UI (English + Georgian) | ✅ Done |
| Tutor profile data fetching | ✅ Done |
| Chat panel with Supabase realtime | ✅ Done |
| Dialog and UI polish | ✅ Done |
| Homework lifecycle: create / submit / grade / shared library | ✅ Done |
| Video calls (LiveKit SFU) + collaborative whiteboard (TLDraw) | ✅ Done |

---

## Sprint 2 Backlog — Priority Order

| Priority | Story | Justification |
|---|---|---|
| 1 | Wire PostHog call-side events | Gates experiment decision rule — blocks whiteboard hypothesis evaluation |
| 2 | Exam syllabus coverage field on tutor profiles | Verbatim user request: S-zk "I want to know if the tutor teaches the physics exam syllabus specifically" |
| 3 | Booking confirmation UX improvement | Usability finding S-gd: "the confirmation felt subtle" |
| 4 | Notification system — email via Supabase Edge Functions | Usability finding T-mg asked about confirmation emails |
| 5 | Student-side review write path | Trust signal for new students choosing a tutor |
| 6 | Group lessons — multi-student LiveKit rooms | Sprint 3 candidate; high effort, lower near-term confidence |

---

## Q3 2026 Themes (July – September)

- Supply growth: onboard 20+ tutors across Math, Physics, Chemistry, Georgian Language
- Retention mechanics: end-of-lesson feedback (1-question survey)
- SEO: server-rendered tutor profile pages for "[subject] tutor [city]" searches
- Payments integration: in-app payment to replace bank-transfer workaround

---

## Q4 2026 — Exam Season (October – December)

- Peak load readiness: LiveKit SFU capacity planning for November exam pressure
- Progress tracking dashboard: lessons completed, homework score trends, exam readiness indicator
- AI homework review improvements: structured feedback tied to Georgian exam marking criteria

---

## 12-Month Targets

| Metric | Target |
|---|---|
| Active tutors on platform | 50 |
| Students completing lessons per month | 200 |
| Monthly recurring revenue | ₾3,150 |
| Tutor referral K-factor | ≥ 0.5 |
| Geographic reach | Tbilisi + Kutaisi + Batumi |

---

## Prioritization Framework

Stories scored using Impact × Confidence ÷ Effort (ICE). See `06-strategy/prioritization-framework.md` for full framework.
