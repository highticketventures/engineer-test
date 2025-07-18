HTV Engineering Take‑Home Assessment

If you can’t ship this, you can’t ship with us. We’re testing your ability to own front‑end, back‑end and DevOps in one shot. Go deep or go home.

🚀 Company Snapshot

High Ticket Ventures (HTV) is a cash‑flow‑first accelerator + PE hybrid. We partner with founders, scale them to 7‑9 figures, then exit. Your code powers that engine.

Vision Doc: https://docs.google.com/document/d/1nyYwJDjSg4Ad88FUk67rlsybJ7bqlLeAJ-5xM4i_Kgc

Product Walkthrough (Loom): https://www.loom.com/share/d08cc6287c2d459fb1f147257b254ec4

Sandboxes (for context)

Area

URL

Founders App

https://htv-portal-sandbox.netlify.app/

Talent

https://v0-talent-highticketventures-com.vercel.app/

Invest

https://v0-invest-highticketventures-com.vercel.app/

Partners

https://v0-partners-highticketventures-com.vercel.app/

These are no‑code prototypes. You’re building the real thing.

🏗️ What You’re Building

A multi‑tenant Request Hub MVP that lets each Portfolio Company (Org) raise requests, auto‑creates Linear issues, and streams status updates in real time.

“Because an employee might be fired but their requests live on, the Org owns the requests. Founders see everything; employees see their own. HTV admins view every Org.”

Functional Requirements

Multi‑Tenant Auth

Firebase Auth (email + magic link) with Org context.

Roles → founder, employee, superAdmin (HTV).

Request Submission

Form: title, category, description, optional attachments.

Persist to Cloud Firestore under /orgs/{orgId}/requests/{requestId}.

Create Linear issue; save issueId.

Real‑Time Status

Linear → Cloud Function webhook → Firestore → client via onSnapshot.

No manual refresh.

Admin Dashboard

Cross‑tenant table.

Org filter + impersonate toggle.

Update status / reassign.

🛠️ Tech Stack (locked‑in)

Layer

Stack

Front‑End

Next.js 15+ (App Router, TypeScript) · Tailwind CSS · shadcn/ui · React Query

Back‑End

Node 18 · Cloud Functions (TypeScript) OR Cloud Run service

Auth

Firebase Authentication (multi‑tenant pattern)

DB / RT

Cloud Firestore (Native) with per‑org security rules

External API

Linear REST + Webhooks

CI/CD

GitHub Actions → gcloud CLI → GCP

IaC

Terraform or Pulumi

No Vercel. Deploy everything to GCP and show the pipeline in your Loom.

Front‑end & back‑end must live in separate folders (apps/web, services/api) or repos.

✅ Mandatory Capabilities

Pixel‑Perfect Figma (we’ll share post‑deposit).

Real‑Time UX (no reload).

E2E Tests — Playwright covering auth, request flow, status update.

CI/CD — lint → test → build → deploy (auto on push).

IaC — spin up the stack from scratch.

Error Monitoring — Sentry for client & server.

Performance — optimistic updates & indexed queries.

Docker — multi‑stage + docker‑compose for local dev.

Deliver anything less → fail.

📦 Deliverables (post once in the Slack thread)

Live URL on GCP (include test creds: founder / employee).

GitHub repo(s) link.

3‑5 min Loom: architecture, code tour, why you’re the founding engineer for HTV.

C4 diagram (PNG/SVG) in /docs.

README (this file) with local setup:

# Clone
$ git clone git@github.com:<you>/htv-request-hub.git && cd htv-request-hub

# Local env
$ cp .env.sample .env.local  # fill Firebase + Linear keys

# Run services
$ docker-compose up --build

💰 Compensation & Timeline





Fee

US $150 (25 % upfront, 75 % on acceptance)

Clock

72 hours from deposit receipt

We’re filtering for owners, not hourly coders. Show you care about the mission.

📝 Getting Started

DM PayPal + preferred email → we invite you to Slack & pay deposit.

Confirm scope + 72 h deadline.

Receive Figma + API tokens.

Build → ask questions in thread so we see your comms.

Post deliverables.

Short follow‑up call if needed.

FAQ

Ship legendary software or ship out.
