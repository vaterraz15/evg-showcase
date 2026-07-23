# Exacting Verus Financial (EVF)

**Precision forged. Unbreakable.**

A full-stack fintech operations platform that handles reconciliation, a double-entry ledger, card issuing, disputes, BSA/AML compliance, cybersecurity, and ML-assisted classification. It is built as one system on Next.js 15, not a set of disconnected tools.

### Live showcase

**https://vaterraz15.github.io/evg-showcase/**

This repository hosts a public showcase page with an interactive, click-through demo running on mock data. It shows how the product works without exposing how it is built. The EVF source code and core algorithms are private.

## What it covers

EVF is organized into thirteen modules that share one schema, one set of design tokens, and route-level access control.

| Module | Route | What it does |
| --- | --- | --- |
| Unified Shell | /dashboard/overview | Navigation shell with a command palette and live operational metrics |
| ClearLedger | /dashboard/ledger | Double-entry general ledger with journal entries and a full audit trail |
| Reconciliation | /dashboard/reconciliation | Multi-tier matching engine with exception queues |
| Resolution Engine | /dashboard/exceptions | Inline exception resolution with an ML-assisted feedback loop |
| Dispute Center | /dashboard/disputes | Reg E, Visa VCR, Mastercard Chargeback, and Amex OMS lifecycles |
| ML Classifier | /dashboard/ml | Transaction classification with opt-out controls and batch mode |
| Sentinel | /dashboard/sentinel | SIEM, encryption keys, RBAC audit, incident response, SOC 2 |
| Watchkeeper | /dashboard/watchkeeper | CIP, OFAC screening, SAR/CTR workflows, CDD queue |
| Card Issuing | /dashboard/card-issuing | Marqeta Core v3 cardholders, cards, controls, GL linkage |
| Rails Reference | /reference/rails | Rail-ID spec across NACHA, IMAD, ARN, TLID, UETR |
| Edge Cases | /reference/edge-cases | Network edge-case catalog |
| Customer Portal | /portal | Small-business books, cash-flow projection, tax package |

## Tech stack

- **Framework:** Next.js 15 App Router with React and TypeScript
- **Database:** PostgreSQL (Neon) with Drizzle ORM
- **Auth:** Clerk with route-level RBAC
- **AI/ML:** Anthropic API
- **Background jobs:** Inngest
- **Cache:** Upstash Redis
- **Storage:** Cloudflare R2 / S3
- **Email:** Resend
- **Card issuing:** Marqeta Core API v3
- **Bank data:** Plaid
- **Hosting:** Vercel

## Highlights

- Eight payment networks modeled with correct rail identifiers, plus double-entry accounting that balances to the penny.
- Multi-tenant schema across seven domains with event-driven jobs and a shared design-token system for white-label theming.
- Reg E disputes, OFAC/CIP screening, SAR/CTR workflows, SOC 2 posture, and an incident-response and disaster-recovery surface.

## About

EVF is a personal engineering project that shows full-stack work across the hardest parts of fintech: money movement, reconciliation, compliance, and card issuing.

Built by Victor A. Terrazas, Exacting Verus Financial LLC.

> This is a demonstration environment. Not a chartered bank. Not FDIC insured. No real customer data. Source code and core algorithms are private.
