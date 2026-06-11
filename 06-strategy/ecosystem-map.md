# Ecosystem Map — TutorLink

**Date:** June 11, 2026

---

## Complements

Products and services that make TutorLink more valuable without competing with it.

| Complement | How it amplifies TutorLink | Status |
|---|---|---|
| Telegram exam-prep groups | Primary organic distribution channel — our content reaches students already pooled in these groups | Active — content being published |
| Instagram / TikTok | Short-form tutor content drives awareness and profile visits | Active — first posts planned |
| Supabase | Auth, Postgres, realtime, storage — removes need to operate infrastructure | Integrated |
| LiveKit Cloud | Managed SFU — enables HD video calls without operating a media server | Integrated |
| PostHog | Product analytics — measures North Star and informs product decisions | Integrated (pageview events live) |
| TLDraw | Open-source collaborative whiteboard synced over LiveKit data channel | Integrated |

---

## Partners

| Partner | What we need | What they get | Status |
|---|---|---|---|
| Exam-prep tutors (Tbilisi / Kutaisi) | Onboard, list subjects, invite existing students | Simplified admin, new student flow, 15% commission vs Preply's 18–33% | **3 tutors confirmed via waitlist (May 2026)** |
| KIU student network | Early student signups and usability testing | Free access to a better tutor-finding tool | **In discussion — 5 students from waitlist, 3 usability test participants** |
| Georgian Ministry of Education exam database | Exam syllabus data to power subject-coverage fields | Attribution / potential official partnership | Identified — not yet approached |
| KIU and Free University Tbilisi student unions | Distribution channel to exam-prep students at scale | Free resource for their members | Identified — approach target: July 15, 2026 |

---

## Threats

| Threat | Likelihood | Counter-strategy |
|---|---|---|
| Preply or iTalki localises for Georgia | Low (12-month window) — Georgian market too small to prioritise for a global platform | Build tutor lock-in via referral loop before they arrive; win the supply side first |
| A Georgian-specific competitor launches | Medium — the gap is visible; a local founder could see it | Execute faster on supply acquisition; lesson history and homework data create switching costs that compound over the exam cycle |
| Tutors leave the platform after acquiring students through it | Medium — tutors have incentive to take relationships off-platform to avoid commission | Whiteboard history, homework records, and payment integration are the lock-in; make the on-platform experience better than off-platform by Sprint 3 |
| LiveKit pricing increases significantly | Low-medium | Architecture supports swapping the media layer (see `03-build/architecture/risk-spikes.md`); self-hosted LiveKit is a documented fallback |
| Supabase free tier limits hit | Low-medium at current scale | Supabase Pro plan is $25/month; cost is accounted for in the 12-month financial model at Month 8+ |

---

## Complementors

Entities that increase the value of the overall exam-prep ecosystem, increasing demand for TutorLink indirectly.

- **Exam preparation book publishers (Bakur Sulakauri):** Students who are actively buying past papers are exactly our ICP. A co-promotion — "use the tutor who helped write these notes" — could put TutorLink in front of motivated exam-prep students at the moment of purchase.
- **Georgian university admissions offices:** Universities that communicate with applicants could include TutorLink as a resource for final-year students. Approach target: August 2026, ahead of the September prep cycle start.
- **Private schools with weak exam-prep programs:** School counsellors who cannot meet all students' tutoring needs become natural referrers.

---

## Strategic Priorities (150 words)

The ecosystem map reveals three near-term strategic priorities. First, deepen the tutor partnership before any competitor arrives — the 3 confirmed tutors are the start of a supply-side moat, but 20 tutors across core exam subjects is the threshold where marketplace liquidity becomes reliably available to any student searching in Tbilisi. Each new tutor brings 3–8 students via the referral loop, making supply acquisition the most efficient growth lever available. Second, convert identified partners (KIU student union, Free University Tbilisi student union) into confirmed distribution channels before the September prep cycle begins — these organisations have the highest density of our exact ICP and cost only time to activate. Target: first meeting by July 15, 2026. Third, begin the relationship with exam-syllabus data sources — even an unofficial mapping of Georgian national exam topics to subject tags would differentiate TutorLink from any competitor and is not replicable without local knowledge.
