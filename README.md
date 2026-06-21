<div align="center">

<img src="assets/hero.png" alt="PixlForge Aegis" width="100%">

# ðŸ›¡ï¸ PixlForge Aegis

### Reputation Defense & Review Intelligence â€” *compliance-first*

*Detect coordinated review attacks. Flag, respond, and prove ROI â€” under hard, code-enforced legal guardrails.*

[![Next.js](https://img.shields.io/badge/Web-Next.js_App_Router-000000?logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/API-FastAPI-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Claude](https://img.shields.io/badge/AI-Claude-3b82f6)](https://www.anthropic.com/)
[![Multi-tenant](https://img.shields.io/badge/SaaS-Multi--tenant-22c55e)]()
[![License](https://img.shields.io/badge/License-Proprietary-1f2937)](#-license)

</div>

> **Compliance first.** Aegis never claims guaranteed review removal. "Flag" = *submit to the platform for policy review; the platform decides.* It only ever acts on a business's **own** Google Business Profile, and **never** touches positive or neutral reviews.

---

## ðŸŽ¬ ~58-second demo

> **â–¶ [Watch the narrated walkthrough â†’](assets/aegis-teaser.mp4)** *(AI-narrated + subtitled)*

<div align="center">

[<img src="assets/screenshots/05-landing.png" alt="Watch the demo" width="80%">](assets/aegis-teaser.mp4)

</div>

<video src="https://github.com/Namanjain723/pixlforge-aegis/raw/main/assets/aegis-teaser.mp4" controls width="100%"></video>

---

## ðŸ’¡ What it does

A business under a **coordinated review attack** â€” a burst of fake one-star reviews from brand-new accounts â€” has almost no legitimate way to respond fast. Aegis gives them one: it detects the attack with AI, assembles the evidence Google actually needs, flags the offending reviews *through the proper policy channel*, and replies to the genuine ones with on-brand AI â€” all while a code-enforced guardrail layer guarantees it never crosses an ethical or legal line.

---

## âœ¨ What's inside

| Module | Status |
|---|---|
| Multi-tenant workspaces + RBAC (Owner / Manager / Agency-Admin / Viewer) | âœ… Live |
| AI fake-review + **coordinated-attack detection** (Claude + free heuristics) | âœ… Live |
| **Reputation Health Score** (live gauge) | âœ… Live |
| **Action Engine** â€” Manual / Approve-each / Auto, with hard guardrails + audit log | âœ… Live |
| Approval Inbox + **auto-tier consent flow** | âœ… Live |
| **Evidence Builder** (PDF) + AI **Response Studio** + flag-status tracking | âœ… Live |
| Client dashboard Â· Marketer trends Â· **CEO console** (MRR / churn / plans) | âœ… Live |
| Billing plans + **plan gating** + GST-compliant invoices | âœ… Live (manual mode) |
| **Hindi / English** UI toggle Â· **PWA** Â· Monthly Reputation Report PDF Â· Reputation Badge widget | âœ… Live |
| **Google Business Profile** OAuth + ownership-verified import + review backfill | âœ… Built (add Google keys) |
| **Razorpay / Stripe** checkout + HMAC-verified webhooks â†’ subscription lifecycle | âœ… Built (add keys) |
| **Email (Resend) + WhatsApp** alert fan-out | âœ… Built (add keys) |

> Every external integration is **fully coded** â€” it only needs the API key to go live. A 46-check all-keys integration test mocks only the network boundary and runs all real app logic end-to-end: **46/46 passing**.

---

## ðŸ“¸ Inside the product

### ðŸ“Š Reputation Dashboard â€” health score + AI-classified reviews
A live Reputation Health Score, plus AI that labels every incoming review **genuine**, **policy violation**, or **coordinated attack** â€” with a code-level guarantee that positive/neutral reviews are never eligible for flagging.

![Dashboard](assets/screenshots/01-dashboard.png)

### ðŸ“¥ Approval Inbox â€” the 3-tier Action Engine
**Manual**, **Approve-each**, or **Auto** â€” and the guardrails are real: auto-tier requires confidence â‰¥ threshold **AND** a mapped policy category **AND** logged consent **AND** under the daily cap, or it falls back to approval. Genuine criticism is never flagged â€” you respond to it instead.

![Action Engine](assets/screenshots/02-action-engine.png)

### âœï¸ Response Studio + Evidence Builder
On-brand AI replies for genuine reviews, and a submission-ready **Evidence PDF** (timeline, duplicate-text diff, policy mapping) for the attacks you flag.

![Response Studio](assets/screenshots/03-response-studio.png)

### ðŸ“ˆ CEO Console â€” run it as a SaaS
Multi-tenant MRR, churn, plan distribution and tenant management â€” agency-ready.

![CEO Console](assets/screenshots/04-ceo-console.png)

### ðŸš€ Public sales demo
A compliance-first landing + live demo to sell the product.

![Landing](assets/screenshots/05-landing.png)

---

## ðŸ”’ Guardrails (enforced in code, not comments)

- Positive / neutral reviews are **never** eligible for flagging.
- **Auto-tier** requires: confidence â‰¥ threshold (default 85) **AND** a mapped policy category **AND** explicit logged consent **AND** under the daily cap â€” else it falls back to approval.
- Every consequential action â†’ an immutable **audit log**.
- No mass-flagging, no fake DMCA, no scraping that submits actions. Monitoring-only for non-API platforms.

---

## ðŸ—ï¸ Architecture (hybrid, low-cost to host)

```
apps/
  api/   FastAPI (Python) Â· SQLAlchemy Â· APScheduler Â· ReportLab Â· Anthropic (Claude)
  web/   Next.js (App Router, TypeScript) Â· Tailwind Â· Recharts Â· PWA Â· i18n
```

- **DB:** SQLite locally (zero setup) â†’ Postgres in prod via `DATABASE_URL`.
- **No Redis / Celery** â€” in-process APScheduler keeps hosting to a single small instance + cheap Postgres.
- **Secrets:** everything blank falls back to safe demo/mock behaviour, so the app always runs. Real keys live only in a local `.env` (never committed).

---

## ðŸ§­ Roadmap to "live"

1. **Now:** sell with the demo + run AI live with an Anthropic key.
2. **~1 month:** Google Cloud + GBP API approved â†’ flip on real OAuth + review sync (slot ready).
3. **When ready:** add Razorpay / Stripe keys to automate billing (manual GST invoicing works today).

---

## ðŸ‘¤ Author

**Naman Jain** â€” PixlForge Studio
ðŸ“§ [info@pixlforgestudio.in](mailto:info@pixlforgestudio.in)
ðŸ”— [github.com/Namanjain723](https://github.com/Namanjain723)

## ðŸ“„ License

Â© PixlForge Studio. All rights reserved. This public repository is a **showcase** â€” documentation, screenshots and the demo video only. The full source is private and the product is proprietary.

---

<div align="center"><sub>PixlForge Aegis â€” reputation defense, done right.</sub></div>
