# Product Overview

## The problem

Traditional uptime monitors only tell you whether a server responded to a
ping. They miss the failures that actually hurt users and businesses most:
a broken layout, a login form that silently stopped working, a checkout page
that renders blank, or a certificate that's about to expire. Teams end up
either flying blind on these issues or drowning in noisy, low-signal alerts.

## The approach

WebPatrolz visits each monitored site the way a real visitor would — in an
actual browser, on a schedule — and evaluates it across multiple dimensions
in a single pass:

1. **Availability & performance** — is it up, and how fast does it respond?
2. **Visual integrity** — does it look the same as last time, or did
   something break/disappear?
3. **Functional integrity** — do critical interactive elements (like a
   login form) still work?
4. **Security & infrastructure health** — is the SSL certificate valid, is
   DNS healthy, are basic security headers present?

The result is condensed into one clear health report per check, with
incidents automatically opened and tracked when something goes wrong —
rather than a wall of disconnected alert emails.

## Who it's for

- **Individual site owners / freelancers** who want more than a ping check
  without paying for enterprise observability tooling
- **Small teams** who want shared visibility, a public status page for their
  customers, and integration with tools they already use (Slack, Discord)
- **Agencies** managing many client sites who need to catch visual/
  functional regressions quickly, not just downtime

## Product tiers (summary)

WebPatrolz is structured as a tiered SaaS product:

- **Free** — core monitoring, screenshots, visual diff, basic alerting
- **Pro** — shorter check intervals, more monitors, AI-assisted incident
  summaries, alert escalation, weekly reports, SEO/content analysis
- **Business** — everything in Pro plus auto-drafted postmortems,
  auto-recovery webhooks, and response-time anomaly detection

Exact limits and pricing are finalized separately and available on request.

## What makes it different

- **Real-browser checks, not just pings** — catches an entire category of
  failure invisible to traditional uptime monitors
- **One health report, not alert spam** — designed around signal, not noise
- **Graceful degradation by design** — optional third-party integrations
  (email delivery, media storage, AI summaries) all have safe, fully
  functional fallbacks, so the product works well even in a minimal
  deployment
- **Built to scale horizontally** — the check-execution layer is designed
  to scale independently of the web application under load

---

For architecture and technical implementation details, qualified partners
and investors can request access to the private engineering repository and
full technical/business report.
