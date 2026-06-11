# Prioritization Framework — TutorLink

**Date:** June 11, 2026

---

## Framework: Impact × Confidence ÷ Effort (ICE)

| Axis | What it measures | Scale |
|---|---|---|
| **Impact** | Expected effect on the North Star (weekly completed lessons) or a directly leading metric | 1 (negligible) → 5 (massive) |
| **Confidence** | Quality of evidence supporting the impact claim | 1 (pure guess) → 5 (measured data) |
| **Effort** | Engineering days to ship | 1 (≥ 2 weeks) → 5 (< 1 day) |

**Priority score = (Impact × Confidence) / Effort**

Anything scoring < 2 is parked until confidence improves. Anything scoring ≥ 6 goes into the next sprint.

---

## Applied to Sprint 2 Backlog

| Story | Impact | Confidence | Effort | Score | Reasoning |
|---|---|---|---|---|---|
| Wire PostHog call-side events | 5 | 5 | 4 | **6.25** | Blocks experiment decision rule — evidence = experiment design already written |
| Exam syllabus field on tutor profiles | 4 | 5 | 3 | **6.67** | Verbatim user request S-zk; effort = schema field + UI |
| Booking confirmation UX fix | 4 | 5 | 5 | **4.00** | Usability finding S-gd; effort is a single UI change |
| Notification system (email) | 4 | 4 | 2 | **3.20** | Usability finding T-mg; effort = Supabase Edge Function |
| Student review write path | 3 | 4 | 3 | **4.00** | Standard marketplace feature; no direct user request |
| Group lessons | 4 | 3 | 1 | **1.20** | Parked — high effort, lower near-term confidence |

---

## Evidence Quality Ladder (Confidence scores)

| Score | Evidence type |
|---|---|
| 5 | Measured PostHog data or A/B test result |
| 4 | Verbatim user quote from interview or usability test |
| 3 | Observed user behaviour during usability session (no explicit quote) |
| 2 | Team belief based on domain knowledge |
| 1 | Assumption with no user evidence |

---

## What This Framework Does Not Do

It does not replace judgment. A high ICE score story that contradicts a strategic priority should be questioned before it enters the sprint. Non-product work (reliability, security, legal compliance) is not scored on ICE — it is treated as a fixed commitment and scheduled separately.
