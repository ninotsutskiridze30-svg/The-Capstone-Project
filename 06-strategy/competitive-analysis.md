# Competitive Analysis — TutorLink

**Team:** TutorLink Team
**Product:** TutorLink
**Date:** June 11, 2026
**Version:** 1.0 — builds on `01-discovery/synthesis/competitive-landscape-seed.md`

---

## Competitor Matrix

Score 0–5: 0 = absent, 5 = excellent/market-leading. Own product scored honestly.

| Dimension | TutorLink | Preply | iTalki | Tutorful | Superprof | WhatsApp (status quo) |
|---|---|---|---|---|---|---|
| Georgian-language UI | **5** | 0 | 0 | 0 | 1 | 3 |
| National exam syllabus coverage | **5** | 0 | 0 | 1 | 0 | 0 |
| Integrated video lesson | **5** | 5 | 5 | 0 | 0 | 0 |
| Collaborative whiteboard | **5** | 0 | 0 | 0 | 0 | 0 |
| Homework and AI grading | **5** | 0 | 0 | 0 | 0 | 0 |
| Commission rate (lower = better) | **4** | 1 | 4 | 2 | 5 | 5 |
| Verified tutor profiles and reviews | 2 | 5 | 5 | 5 | 3 | 0 |
| Mobile booking experience | 4 | 5 | 4 | 4 | 2 | 1 |
| Brand recognition in Georgia | 1 | 2 | 2 | 0 | 0 | 5 |

**Scoring notes:** TutorLink's review system (2) reflects MVP state — the write path for student reviews is Sprint 2 work. WhatsApp scores 5 on brand recognition because it is the de facto tool Georgian students use. Superprof scores 5 on commission because it is a directory model with a tutor subscription, not a per-lesson fee.

---

## Competitor Profiles

### Preply
**Type:** Direct competitor
**Description:** Global tutoring marketplace with 1:1 video lessons in 50+ subjects and 150+ languages. Strong brand in Europe and North America.
**Primary strengths:** Large tutor supply globally; strong video infrastructure; established trust and review system.
**Primary weaknesses:** English-first platform; commission 18–33% (drops as tutor earns more, but starts very high); no Georgian exam-syllabus context.

### iTalki
**Type:** Indirect competitor (language learning focus)
**Description:** Language learning marketplace; strong in English, Chinese, Spanish, but positioned for conversational practice not curriculum exam prep.
**Primary strengths:** 15% commission (aligned with ours); large supply for popular languages.
**Primary weaknesses:** Designed for language acquisition, not curriculum-based exam prep; no Georgian national exam context.

### Tutorful (UK)
**Type:** Indirect competitor (different geography)
**Description:** UK tutoring marketplace strong for GCSE/A-Level prep. 22% commission.
**Primary strengths:** Strong local brand in UK; good subject filters for UK curriculum.
**Primary weaknesses:** Entirely UK-centric; no Georgian presence; no integrated lesson experience (connects tutor and student, then they use Zoom).

### Superprof
**Type:** Indirect competitor (directory model)
**Description:** Directory in 40+ countries — tutors list themselves, students contact directly. No booking or payment infrastructure.
**Primary strengths:** Zero commission per lesson (tutors pay a subscription); broad international presence.
**Primary weaknesses:** No integrated lesson experience; same fragmentation problem as WhatsApp just with a website.

### WhatsApp / Telegram (status quo)
**Type:** Substitute (the current behaviour)
**Description:** How all Georgian exam-prep tutor discovery actually happens. Students post in group chats, collect names, contact individually.
**Primary strengths:** Zero cost; existing social trust.
**Primary weaknesses:** Stale information; manual serial process; no booking, payment, or lesson infrastructure.

---

## Synthesis — 200 Words

**Porter's Five Forces — highest threat:** Threat of New Entrants. The codebase for a tutoring marketplace is not technically novel — a well-funded competitor could build the same feature set in 3–4 months. The barrier is not technology; it is the two-sided network. Our moat window is the time between now and when the marketplace achieves enough liquidity that switching costs emerge naturally.

**Most defensible gaps:** Two dimensions create the strongest defensible position. First, Georgian-language product quality with exam-syllabus coverage — Preply and iTalki could add Georgian as a locale, but localising for a specific national exam curriculum requires deep local knowledge a remote team cannot replicate quickly. Second, the integrated lesson experience (video + whiteboard + homework in one session) — no competitor currently offers this, and building it while also winning the Georgian market would require prioritising a market too small for any global platform's roadmap.

**What would close the gaps:** A Georgian-focused investor backing a team with existing tutor relationships in Tbilisi could replicate the supply side in 6 months. The network effect — tutors bringing their existing students onto the platform — is our primary defence, which is why the tutor referral loop is Priority 1 in the GTM plan.
