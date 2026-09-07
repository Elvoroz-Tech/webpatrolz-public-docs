# WebPatrolz — Intelligent Website Monitoring Platform

> Real-browser uptime, visual regression, and form-health monitoring — with one clear health report instead of a flood of alerts.

<!--
  BADGES — uncomment / edit once you have real links.
  These are just examples; swap in a badge generator (shields.io) if you want live status badges.

  ![Status](https://img.shields.io/badge/status-in%20development-yellow)
  ![License](https://img.shields.io/badge/license-proprietary-lightgrey)
-->

**🔗 Live demo:** _[coming soon — add link here]_
**🎥 Demo video:** _[coming soon — add YouTube / Loom link here]_

---

## Overview

Most uptime monitors only check whether a server responds to a ping. **WebPatrolz goes further** — it visits every monitored website in a real, headless browser on a schedule and checks it the way an actual visitor would experience it:

- Confirms the site is reachable and measures real response time
- Takes a full-page screenshot and automatically compares it to the previous one to catch visual regressions (broken layouts, missing sections, silently-disappeared content)
- Tests that critical page elements still function (e.g. does the login form still have a working email field, password field, and submit button)
- Checks SSL certificate validity and expiry, DNS health, and security headers
- Rolls all of this into a single, clear health report instead of noisy, disconnected alerts

Built as a production-shaped, multi-service platform with real-time updates, team collaboration, public status pages, and a paid-tier automation suite.

---

## ✨ Key Features

### For end users
- Secure signup with email verification and JWT-based authentication
- Add monitors with configurable check frequency and full check history
- Visual-diff detection with an ignore-regions editor (mask dynamic content like banners or clocks)
- Automated form/login-flow testing
- SSL certificate, DNS, and security header diagnostics
- Real-time in-app notifications plus instant or digest email alerts
- Slack, Discord, and generic webhook integrations
- Incident tracking with a public-facing timeline
- Customizable public status pages
- Maintenance windows to suppress alerts during planned downtime
- Team/organization support with email invites
- API keys for CI/CD and scripted access

### For admins
- Dedicated admin panel with analytics dashboards and date-range filtering
- SSL/domain expiry watchlist across all monitors
- User management and audit logging

### Paid-tier automations
- AI-assisted incident root-cause summaries
- Automated alert escalation policies
- Weekly rollup reports
- Auto-drafted postmortems
- Auto-recovery webhooks
- Response-time anomaly detection
- On-page SEO/content analysis

### Built for resilience
The monitoring engine is designed to degrade gracefully rather than break — automatic retries before marking a site down, sensible fallbacks when optional third-party services aren't configured, and a self-healing browser worker.

---

## 🏗️ Architecture (high level)

```
                     ┌──────────────────────────┐
   Browser ───────▶ │    Web Frontend          │
                     │  (Next.js / TypeScript)  │
                     └───────────┬──────────────┘
                                 │
                     ┌───────────┴─────────────┐
                     │                         │
                     ▼                         ▼
          ┌──────────────────────┐     ┌───────────────────────────┐
          │   Auth Service       │     │      Core Service         │
          │  Accounts, sessions  │     │  Monitoring pipeline,     │
          │  Orgs, API keys      │     │  incidents, status pages, │
          │  Admin auth          │     │  integrations, realtime   │
          └──────────┬───────────┘     └────────────┬──────────────┘
                     │                              │
                     └──────────────┬───────────────┘
                                    ▼
                          ┌────────────────────┐
                          │     PostgreSQL     │
                          └────────────────────┘
```

The platform is split into a frontend and two backend services behind a single origin, backed by a shared PostgreSQL database. The monitoring pipeline itself (scheduler → browser check → visual/form analysis → report) runs as an independently scalable worker layer, with an optional queue-backed mode for horizontal autoscaling under load.

*(Full internal architecture, database schema, and implementation details are kept in the private engineering repository.)*

---

## 🧰 Tech Stack

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS, real-time updates via WebSockets
- **Backend:** Node.js, Express, TypeScript, Prisma ORM
- **Monitoring engine:** Headless browser automation (Playwright), image-diffing
- **Database:** PostgreSQL
- **Infrastructure:** Docker, Kubernetes-ready with autoscaling support for the check-execution layer
- **Email & storage:** Third-party email delivery and media storage, both with safe local fallbacks

---

## 📸 Screenshots

_Screenshots coming soon — see [screenshots/README.md](screenshots/README.md) for the exact pages that will be captured here._

<!--
  Once you have images in /screenshots, replace this block with something like:

  ### Dashboard
  ![Dashboard](screenshots/dashboard.png)

  ### Monitor detail & visual diff
  ![Monitor detail](screenshots/monitor-detail.png)
-->

---

## 🎬 Demo Video

_A walkthrough video / GIF demo will be embedded here soon._

<!--
  Once you have a video, embed it like this:

  [![Watch the demo](screenshots/video-thumbnail.png)](https://youtube.com/your-video-link)
-->

---

## 📄 Documentation

- [Product overview & feature notes](docs/FEATURES.md)
- [Security posture (summary)](docs/SECURITY_OVERVIEW.md)
- [Roadmap](docs/ROADMAP.md)

> Note: this repository contains product documentation only. The application source code lives in a private repository and is available to qualified partners and investors under NDA.

---

## 📬 Contact

Interested in a demo, partnership, or investment? 

- Email - contact@elvoroz.com
- Website - https://elvoroz.com/


---

## License

Proprietary — all rights reserved. This repository and the underlying product are not open source.
