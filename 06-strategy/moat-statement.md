# Moat Statement — TutorLink

**Team:** TutorLink Team
**Date:** June 11, 2026
**Framework:** Helmer's Seven Powers

---

## The Power

**Primary Helmer Power claimed:** Network Effects (two-sided marketplace network effect)

---

## The Mechanism

Every tutor who joins TutorLink and invites their existing private students makes the platform more valuable to those students — who can then find additional tutors for other subjects — which in turn makes the platform more attractive to new tutors seeking a larger student base. As the number of tutors in a given subject increases, students have better matching options; as the student base grows, tutors have higher utilisation rates and less admin overhead. Each tutor who onboards brings a cohort of 3–8 students who would otherwise never have heard of TutorLink, bootstrapping demand alongside supply in a way that a competitor entering later cannot easily replicate.

---

## The Evidence

**Evidence 1:**
- Type: Waitlist data showing two-sided demand signal
- Description: 10 waitlist signups from a single evening of outreach on May 18, 2026: 5 students and 5 tutors. Subject liquidity table shows Math and Physics already have multiple tutor-student pairings possible at MVP scale.
- Repository link: `04-gtm/traction/waitlist.csv` and `04-gtm/traction/README.md`

**Evidence 2:**
- Type: Growth loop quantification
- Description: Tutor referral loop diagram with K-factor arithmetic. Each tutor is modelled to bring 3–8 students via referral link. The loop compresses CAC to ₾1.32 — the lowest possible because the tutor does the acquisition work. At K > 1 the loop is self-sustaining.
- Repository link: `04-gtm/loops-and-moats.md`

**Evidence 3:**
- Type: Switching cost evidence (qualitative)
- Description: Once a tutor has onboarded their students, lesson history, whiteboard snapshots, homework records, and payment history are stored on TutorLink. Moving to a competing platform means losing this continuity — a real cost for both tutor and student documented as a design intention in the system architecture.
- Repository link: `03-build/architecture/system-design.md`

---

## Honest Caveat — Moat Hypothesis Label

This power is a hypothesis at MVP scale. With 3 confirmed tutors and 9 external student signups (May 2026), the network is not yet self-sustaining. The evidence above demonstrates the mechanism is in place and the early signal is promising — it is not yet measured at the scale where the network effect becomes structurally defensible.

---

## Path Forward (60 days)

Launch tutor referral links in Sprint 2 (target: July 1, 2026). Run the referral loop for 60 days through the summer exam preparation period. Measure K-factor from PostHog `signup_source = referrer_tutor_id` events. If K ≥ 0.3 (each tutor brings 0.3+ new students per cycle), the network effect is confirmed as operational. Update this document with measured K-factor by August 31, 2026. Simultaneously approach KIU and Free University Tbilisi student unions as confirmed distribution partners — named organisations, specific ask, target by July 15, 2026.
