# TutorLink — Tutoring Platform for Georgian Exam-Prep Students

> Find a verified tutor, book a session, attend a real lesson with a shared whiteboard, submit homework — in Georgian or English.

---

## Problem

Georgian high-school students preparing for the national university entrance exam (ერთიანი ეროვნული გამოცდები) spend days finding an exam-prep tutor because the entire discovery process is fragmented across WhatsApp and Telegram group chats, with no visibility into tutor availability, rates, or exam-topic coverage.

---

## Live Product

**[tutoring-lyart.vercel.app](https://tutoring-lyart.vercel.app/en)**

---

## Demo Video

09-final/Recording 2026-06-11 204739.mp4
---

## Team

| Name | Role |
|---|---|
| Luka Khimshiashvili | Tech Lead |
| Nino Tsutskiridze | Program Lead |
| Lizi Margvelashvili | Discovery Lead |
| Mari Janjghava | Discovery Lead |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Next.js 16.2 (App Router) + React 19 + TypeScript 5 |
| Styling | Tailwind CSS v4 + shadcn/ui + Radix UI |
| Database and Auth | Supabase (Postgres + Row-Level Security + Realtime) |
| Video and Whiteboard | LiveKit Cloud SFU + TLDraw (synced over LiveKit data channel) |
| Analytics | PostHog Cloud |
| i18n | next-intl (English + Georgian) |
| Deployment | Vercel |

---

## Setup Instructions

**Prerequisites:** Node.js 20+, yarn, Supabase project, LiveKit Cloud account, PostHog Cloud account

```bash
git clone https://github.com/lukakh1/tutoring
cd tutoring
yarn install
```

Copy `.env.example` to `.env.local` and fill in:
```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
LIVEKIT_API_KEY=
LIVEKIT_API_SECRET=
NEXT_PUBLIC_LIVEKIT_URL=
NEXT_PUBLIC_POSTHOG_KEY=
NEXT_PUBLIC_POSTHOG_HOST=
```

```bash
yarn dev
# Open http://localhost:3000/en
```

Apply DB migrations: `supabase db push`

---

## Architecture Overview

Server-rendered Next.js monolith (Vercel) → Supabase BaaS (Postgres, auth, storage, realtime) → LiveKit Cloud SFU (video + whiteboard data channel).

Full details: [03-build/architecture/system-design.md](03-build/architecture/system-design.md)

Diagram: [03-build/architecture/architecture-diagram.png](03-build/architecture/architecture-diagram.png)

---

## Licence

MIT — see [LICENSE](LICENSE)

---

*CS-PD-2026 | Spring 2026 | Kutaisi International University | Instructor: Zeshan Ahmad*
