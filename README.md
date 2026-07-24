# Exacting Verus Financial (EVF)

**Precision forged. Unbreakable.**

EVF is a fintech operations platform I'm building as a personal project. It covers reconciliation, a double-entry ledger, card issuing, disputes, BSA/AML compliance, security operations, and ML-assisted transaction classification, all on one schema inside a single Next.js 15 app.

## Live showcase

**https://vaterraz15.github.io/evg-showcase/**

This repository contains the public showcase page and nothing from the platform itself. The page has a click-through demo of all twelve modules running on mock data. The EVF source code and core algorithms are private.

Things worth trying in the demo:

- Press Ctrl+K (Cmd+K on a Mac) to open the command palette and jump between modules.
- Click into table rows to expand journal entry legs, exception details, and card controls.
- The demo's address bar follows the same route structure as the real app, and you can deep-link to any module, for example `#/dashboard/ledger`.
- The classifier view accepts your own input. It runs a small keyword stand-in in the browser, since the real model pipeline stays private.

Wherever the real logic would appear, the demo shows a lock notice naming what was left out: matching tolerances, confidence gates, posting rules, detection thresholds, prompt design.

## Modules

| Module | Route | What it does |
| --- | --- | --- |
| Unified Shell | /dashboard/overview | Navigation shell with a command palette and operational metrics |
| ClearLedger | /dashboard/ledger | Double-entry general ledger with journal entries and an audit trail |
| Reconciliation | /dashboard/reconciliation | Multi-tier matching engine with exception queues |
| Resolution Engine | /dashboard/exceptions | Inline exception resolution with an ML-assisted feedback loop |
| Dispute Center | /dashboard/disputes | Reg E, Visa VCR, Mastercard Chargeback, and Amex OMS lifecycles |
| ML Classifier | /dashboard/ml | Transaction classification with opt-out controls and batch mode |
| Sentinel | /dashboard/sentinel | SIEM, encryption keys, RBAC audit, incident response, DR, SOC 2 |
| Watchkeeper | /dashboard/watchkeeper | CIP, OFAC screening, SAR/CTR workflows, CDD queue |
| Card Issuing | /dashboard/card-issuing | Marqeta Core v3 cardholders, cards, controls, GL linkage |
| Rails Reference | /reference/rails | Rail-ID spec across NACHA, IMAD, ARN, TLID, UETR |
| Customer Portal | /portal | Small-business books, auto-categorization, tax package, dispute intake |
| Money Watch | /portal/money-watch | Alerts when expected money doesn't arrive, plus a 13-week cash projection |

## Tech stack

- Next.js 15 App Router, React, TypeScript
- PostgreSQL (Neon) with Drizzle ORM
- Clerk for auth, with route-level RBAC
- Anthropic API for classification
- Inngest for background jobs
- Upstash Redis, Cloudflare R2/S3, Resend
- Marqeta Core API v3 for card issuing, Plaid for bank data
- Hosted on Vercel

## Why I built it

Most portfolio projects avoid the parts of fintech that are actually hard: money movement, reconciliation, compliance, and card issuing. I wanted one codebase that takes those on together. Eight payment networks are modeled with their real rail identifiers, the accounting balances to the penny, and the compliance surfaces follow the actual regulatory clocks, from Reg E provisional credit deadlines to the SAR filing window.

Built by Victor A. Terrazas, Exacting Verus Financial LLC.

> This is a demonstration environment. Not a chartered bank. Not FDIC insured. No real customer data. Source code and core algorithms are private.
