# Case Study — TutorLink: Building a Tutoring Platform for Georgian Exam-Prep Students

**CS-PD-2026 | Demo Day | June 11, 2026**
**Author:** Luka Khimshiashvili (Tech Lead)

---

## The Problem We Started With

In March 2026 our team began customer discovery with no product hypothesis. Ten customer interviews later, the problem was clear: Georgian high-school students preparing for the national university entrance exam (ერთიანი ეროვნული გამოცდები) have no structured way to find, book, or attend sessions with exam-prep tutors. The entire process — finding tutors, agreeing on rates, scheduling, teaching, and submitting homework — happens across WhatsApp, Telegram, Zoom, and bank transfer, with none of it connected.

The most memorable verbatim quote: *"I spent close to a week trying to find a physics tutor. Two were already full, one had raised their rate, and one taught at times that conflicted with my lectures."* — Interview P3

That quote became our benchmark. Any solution had to reduce that week of searching to minutes.

---

## Discovery — What Surprised Us

We expected to find that students could not find tutors at all. What we found was more nuanced: tutors existed and were findable, but the information reached students stale. By the time a forwarded recommendation arrived, the tutor was often already fully booked. The problem was not supply — it was real-time availability and structured information.

We also learned that tutors had their own pain: managing 5–8 private students across Telegram scheduling threads, WhatsApp homework submissions, and bank transfer confirmations was genuinely exhausting. This shaped the whole product — we were not building a student-facing discovery tool. We were building an integrated lesson platform that solved the tutor's admin problem and the student's discovery problem simultaneously.

---

## Design — The Whiteboard Decision

After usability testing three wireframe iterations with 5 real users, we committed to four core flows: Find, Book, Learn, and Improve. The whiteboard was the highest-risk design decision. Participant S-zk told us, unprompted, that a shared whiteboard would make the platform worth using over a plain Zoom call. We shipped it in Sprint 1 as the core risk spike.

On May 8 we chose LiveKit SFU over mesh WebRTC after a risk spike showed mesh would not support the Sprint 2 group-lesson use case. The whiteboard syncs over the LiveKit data channel — one fewer moving part, shared auth with the call. Decision documented in `03-build/architecture/risk-spikes.md`.

---

## Build — One Sprint, Ten Stories, a Deployed MVP

Sprint 1 ran April 23 – May 13, 2026. Ten user stories shipped: auth, role-specific registration, booking flow, bilingual UI (EN + Georgian), real-time chat, homework lifecycle with AI review, HD video calls via LiveKit SFU, and collaborative whiteboard via TLDraw.

The deployed URL went live before the Sprint 1 deadline and has been running without downtime since.

---

## GTM — Going to Market with Zero Budget

Three acquisition channels, all zero cash spend: tutor referral loop (CAC ₾1.32), Telegram exam communities (CAC ₾8 time-only), Instagram/TikTok content (CAC ₾15.50 blended). One evening of outreach on May 18 produced 10 waitlist signups: 5 students + 5 tutors — two-sided traction from the first push.

---

## What We Would Do Differently

Start the waitlist earlier (Week 6, not Week 12). Build the tutor referral link in Sprint 1 to start measuring K-factor. Write standup logs the same day, not retroactively.

---

## What We Are Proud Of

The product works end-to-end, in Georgian, on any device. No competitor offers this. LTV:CAC is 143:1 on the referral channel. We set out to reduce a week of searching to minutes. The platform does that.

---

## Metrics at Demo Day

| Metric | Value |
|---|---|
| Live URL | tutoring-lyart.vercel.app |
| Sprint 1 stories shipped | 10/10 |
| DB migrations in production | 12 |
| Waitlist signups | 10 (5 students + 5 tutors) |
| Usability test participants | 5 |
| Student LTV | ₾252 |
| Blended cash CAC | ₾1.06 |
| LTV:CAC (referral channel) | 143:1 |
