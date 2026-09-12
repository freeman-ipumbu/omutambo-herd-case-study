# Omutambo Herd Operations

![Omutambo Herd Operations](https://raw.githubusercontent.com/freeman-ipumbu/omutambo-herd-case-study/main/omutambo-mark.svg)

**A Namibia-first livestock operations workspace for cattle owners, farm managers and field teams.**

Omutambo turns scattered notebooks, spreadsheets, WhatsApp messages and memory into one reviewable herd record. It connects animal identity, health, breeding, grazing, water, movements, tasks, costs and evidence without hiding uncertainty or replacing the owner, manager or qualified veterinarian.

> This is a public product case study. The working application, private deployment configuration, credentials, customer records and operational data remain separate. All examples in this repository are fictional presentation material.

<!-- RELEASE-STATUS:START -->
## Release status

**public-launch-1 — Public website live; owner-managed invitation access enabled and verified.**

Current deployed system: Public front page at https://omutambo.pages.dev with protected sign-in; hosted second-email identity verification, invitation activation, isolated demo save, viewer restriction, activation replay rejection and existing-session revocation verified; owner administration, photographs and backup export verified.

Review scope: Invitation-only test programme; each tester has a separate demo workspace; only the owner can access live farm records.

Verification: **88 automated checks passed** in the released application build. These cover record handling, signed identity, invitation activation and replay, expiry, revocation, role boundaries, isolated workspaces, backups and browser-draft behaviour. Local browser review also exercised the owner invitation form. Hosted owner administration, invitation creation/revocation, photograph save/reload and backup export have also been verified. Hosted second-email activation, isolated demo saving, viewer restrictions, consumed-code rejection and existing-session revocation have also passed.

Operating limits: 10 MiB per workspace including photographs; latest 20 saved revisions; up to 200 access records.

Public website: https://omutambo.pages.dev. The owner controls invitation access through the hosted administration console.
<!-- RELEASE-STATUS:END -->

## My role

**Freeman Ipumbu — Product owner, designer, systems engineer and researcher**

I framed the operating problem, designed the information architecture, built the working product, shaped the Namibia-first visual language, added versioned cloud persistence and photo handling, deployed the private Cloudflare application and owner access management and wrote the production hardening plan.

## The problem

Cattle operations are continuous, distributed work. A tag is checked in the kraal, a treatment is recorded beside a crush pen, a breeding event is remembered during a call, a water point is inspected in the field and a cost lands in a receipt book. When those facts cannot be joined reliably, owners lose time and confidence exactly when a decision needs evidence.

Omutambo explores a more dependable operating picture: every animal has an identity, every field event has a time and owner, every exception stays visible, and every prompt remains reviewable by the people with authority to act.

## Product response

- Cattle register with tag, name, breed, class, age, camp and status.
- Resized animal photographs attached from a phone or computer and included in complete backups.
- Click-through animal profiles that bring identity, current camp, status and review context together.
- Health and treatment ledger for vaccinations, follow-ups, drenches and vet notes.
- Breeding and calving register for service, pregnancy checks, expected dates and calving outcomes.
- Grazing camp and water-point view for occupancy, trough checks and field notes.
- Movement register for traceability between camps and handling events.
- Task queue for assigning field actions and closing them after verification.
- Cost ledger in NAD across veterinary care, feed, transport and handling.
- Searchable records with clear empty, stale and offline language.
- JSON and CSV exports plus print mode for handovers, vet visits and paper files.
- Owner device drafts with visible cloud acknowledgements and conflicting-write protection.
- Separate demo and live workspaces backed by versioned cloud records.
- Prepared owner console for named invitations, expiring tester/viewer permissions, revocation and access history.

## Design science approach

The work follows the same evidence-led discipline I use across NamAir and NamMar while keeping the livestock domain purpose-built:

1. **Problem framing** — understand the operational cost of fragmented herd records.
2. **Objectives** — create one trustworthy record without adding field complexity.
3. **Artefact design** — connect animal identity to events, places, people and evidence.
4. **Demonstration** — build realistic owner, manager, field-worker and vet-review journeys.
5. **Evaluation** — test clarity, responsive behavior, offline language, exports, photo handling and data boundaries.
6. **Hardening** — define identity, tenant isolation, audit, storage, sync, backup and incident controls before live data.

## Operating principles

- **State must be visible.** Owners should not infer herd or task readiness from silence.
- **Freshness must be explicit.** A local draft, stale server record and current sync state need different labels.
- **Evidence should travel with the record.** Photos, notes, dates and ownership make a field event reviewable.
- **Recommendations need reasons.** Prompts are cues for owner or vet review, never automated diagnoses or approvals.
- **Authority remains human.** The owner, manager and qualified veterinarian remain accountable for decisions.
- **Fallbacks must be honest.** If weather, maps or sync are not configured, the interface says so instead of inventing live values.
- **Production claims stay controlled.** A demonstration is not described as a certified veterinary, financial or regulatory system.

## Namibia-first details

The interface uses Namibian geography in sample records, NAD currency, Southern African date and time language, metric herd units and simple field vocabulary. It is designed for intermittent connectivity and phone-sized screens without assuming continuous broadband or a dedicated data clerk.

The product starts with cattle operations in Namibia while leaving room for other herd types, regional practices, multiple properties and partner workflows after the correct domain and governance work is done.

## Engineering overview

The deployed application combines a responsive browser interface with a Cloudflare Worker API and transactional D1 persistence. The server validates the signed identity and submitted records, rejects stale writes and preserves revision metadata. Complete backups include photographs; CSV exports serve spreadsheet handovers.

The deployed access-management build separates identity verification from the owner's permission decisions. A valid email login alone does not grant a farm workspace. A tester must activate a matching, unexpired, single-use invitation, and every data request checks the current grant. Viewer permissions are enforced by the server. Tester data is scoped to the verified identity, and the live farm remains owner-only.

Authenticated screens are not cached in the deployed build. Owner drafts are scoped to identity; tester drafts stay in the current page until the cloud confirms the save. Access expiry and revocation are checked at each server request. Access history records administrative actions, activations and throttled workspace visits.

## Production path

This is a controlled owner demonstration and test programme. Broader commercial onboarding still needs shared-farm roles, scalable private object storage, monitored budgets and request limits, scheduled independent backups, hosted recovery drills, identity-provider MFA enforcement, incident response and appropriate commercial and data-governance review.

The public narrative distinguishes deployed evidence from prepared features. No security certification, commercial launch readiness or external integration is implied by a passing local test suite.

## Safety and data boundary

All names, tags, animals, dates, costs, camps, treatments and events shown in the demonstration are fictional onboarding data. Omutambo does not diagnose animals, prescribe treatment, approve sales, make financial decisions or replace a qualified veterinarian, owner or manager.

Live weather, map, satellite, market-price and external veterinary integrations are not implied by the demo. Any future provider must show source, timestamp, coverage and limitations at the point of use.

## Repository boundary

This public repository contains the public website assets and product case study. The website links to a separately protected application. It excludes:

- deployable private application source and backend implementation;
- credentials, API keys, tokens and environment variables;
- customer, pilot, owner or livestock records;
- animal photos and private exports;
- database schemas, migrations and internal endpoints;
- private deployment identifiers and operational runbooks.

Please report security concerns privately to [freeman.ipumbu@outlook.com](mailto:freeman.ipumbu@outlook.com), not through a public issue.

---

© 2026 Freeman Ipumbu. Shared for portfolio evaluation and product discussion. No licence is granted to reproduce the product, branding or documentation.
