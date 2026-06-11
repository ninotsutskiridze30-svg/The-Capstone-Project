# SLO Sheet — TutorLink

**Product:** TutorLink — Tutoring Platform for Georgian Exam-Prep Students
**Team:** TutorLink Team
**Date:** June 11, 2026
**Review cadence:** Monthly, or immediately after any SEV1 incident

---

## Glossary

**SLI:** A specific metric we measure. The raw number.
**SLO:** The target we set for an SLI over a time window. An internal commitment.
**Error budget:** The amount of unreliability the SLO allows. Budget = (1 - SLO target) × time window.

---

## SLO 1: Booking Flow Availability

**SLI definition:**
- Metric: Percentage of HTTP POST requests to `/api/bookings` that return a 2xx response within 3 seconds
- Formula: `successful_booking_requests / total_booking_requests × 100`
- Measured by: Vercel function logs (dashboard → Functions → `/api/bookings`); secondary signal: PostHog `booking_confirmed` event
- Measurement frequency: Checked weekly; continuous in Vercel dashboard
- Current measured value: Not yet at statistical scale — no 5xx errors on `/api/bookings` since deployment (May 2026)

**SLO target:**
- Target: 99.5% of booking requests succeed within 3 seconds
- Time window: Rolling 30 days
- Why this target is achievable: Vercel serverless achieves ~99.9% uptime; Supabase free tier achieves ~99.5%. Our SLO is calibrated to the weakest link (Supabase).

**Error budget:**
```
SLO target: 99.5%
Allowed failure rate: 1 - 0.995 = 0.005 = 0.5%

Window in minutes:
30 days × 24 hours × 60 minutes = 43,200 minutes

Error budget:
0.005 × 43,200 = 216 minutes per 30-day window

Equivalent in hours: 216 / 60 = 3.6 hours
```

**Current error budget remaining:** 216 minutes (full budget — no booking incidents since deployment)

---

## SLO 2: Video Call Session Establishment

**SLI definition:**
- Metric: Percentage of LiveKit room-join attempts that result in a connected room state within 10 seconds
- Formula: `successful_room_connections / total_room_join_attempts × 100`
- Measured by: LiveKit Cloud dashboard (Connection Quality metrics); PostHog `video_call_started` event fires on successful connection — absence within 10 seconds of token issuance counts as a failure
- Measurement frequency: Per-session; reviewed weekly in LiveKit dashboard
- Current measured value: Not yet at statistical scale. No failed connections observed during testing.

**SLO target:**
- Target: 99% of room-join attempts establish a connected session within 10 seconds
- Time window: Rolling 30 days
- Why this target is achievable: LiveKit Cloud SLA is 99.9% uptime. We set our SLO at 99% to account for client-side network variability on Georgian mobile networks, which is outside our control.

**Error budget:**
```
SLO target: 99%
Allowed failure rate: 1 - 0.99 = 0.01 = 1%

Window in minutes:
30 days × 24 hours × 60 minutes = 43,200 minutes

Error budget:
0.01 × 43,200 = 432 minutes per 30-day window

Equivalent in hours: 432 / 60 = 7.2 hours
```

**Current error budget remaining:** 432 minutes (full budget — no failed connections since deployment)

---

## Error Budget Policy

When any SLO error budget is exhausted in a given window:

1. No new feature deployments until the window resets or reliability improves
2. Next sprint pivots to reliability work, not feature work
3. Incident review mandatory before the next production push

**Who owns the error budget decision:** Luka Khimshiashvili (Tech Lead)

---

## Severity Definitions

### SEV1: Core flow completely down

**Definition for TutorLink:** No user can complete a booking (booking endpoint returns 5xx for >50% of requests) OR no video call can be established (LiveKit token endpoint returns 500 or LiveKit Cloud is unreachable).

**Response:** Immediate. Check Vercel function logs first; roll back the most recent deploy if the issue started within 30 minutes of a deploy.
**Target time to mitigate:** 1 hour

### SEV2: Degraded experience, core flow partially affected

**Definition for TutorLink:** Some users cannot complete bookings (error rate 1–50% on `/api/bookings`). Or video calls connect but whiteboard TLDraw sync is broken. Or homework file upload fails for specific types. Core flow works for most users.

**Target time to mitigate:** 4 hours during working hours

### SEV3: Minor issue, workaround exists

**Definition for TutorLink:** A non-critical feature is broken (email notifications not sending, single Georgian translation missing). Error rate elevated but below 1% on core endpoints. Performance degraded but within SLO.

**Target time to fix:** Next sprint

---

## On-Call

| Week | On-call |
|------|---------|
| Jun 11–17 | Luka Khimshiashvili |
| Jun 18–24 | Luka Khimshiashvili |

Check the live URL once per day. Create a GitHub issue for any alert, even self-resolving ones.
