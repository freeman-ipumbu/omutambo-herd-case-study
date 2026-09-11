# Omutambo Herd Operations

![Omutambo Herd Operations](https://raw.githubusercontent.com/freeman-ipumbu/omutambo-herd-case-study/main/assets/omutambo-mark.svg)

**A Namibia-first livestock operations workspace for cattle owners, farm managers and field teams.**

Omutambo turns scattered notebooks, spreadsheets, WhatsApp messages and memory into one reviewable herd record. It connects animal identity, health, breeding, grazing, water, movements, tasks, costs and evidence without hiding uncertainty or replacing the owner, manager or qualified veterinarian.

> This is a public product case study. The working application, private deployment configuration, credentials, customer records and operational data remain separate. All examples in this repository are fictional presentation material.

## My role

**Freeman Ipumbu — Product owner, designer, systems engineer and researcher**

I framed the operating problem, designed the information architecture, built the working product, shaped the Namibia-first visual language, added local-first persistence and photo handling, prepared the private Cloudflare test deployment and wrote the production hardening plan.

## The problem

Cattle operations are continuous, distributed work. A tag is checked in the kraal, a treatment is recorded beside a crush pen, a breeding event is remembered during a call, a water point is inspected in the field and a cost lands in a receipt book. When those facts cannot be joined reliably, owners lose time and confidence exactly when a decision needs evidence.

Omutambo explores a more dependable operating picture: every animal has an identity, every field event has a time and owner, every exception stays visible, and every prompt remains reviewable by the people with authority to act.

## Product response

- A cattle register with tag, name, breed, class, age, camp and status.
- Optional animal photographs attached from a phone or computer and retained with the local record.
- Click-through animal profiles that bring identity, current camp, status and review context together.
- Health and treatment ledger for vaccinations, follow-ups, drenches and vet notes.
- Breeding and calving register for service, pregnancy checks, expected dates and calving outcomes.
- Grazing camp and water-point view for occupancy, trough checks and field notes.
- Movement register for traceability between camps and handling events.
- Task queue for assigning field actions and closing them after verification.
- Cost ledger in NAD across veterinary care, feed, transport and handling.
- Searchable records with empty, stale and offline language that is understandable in the field.
- JSON and CSV exports plus print mode for handovers, vet visits and paper files.
- Local-first drafts that remain useful when connectivity drops.
- A zero-dependency local API path for controlled demos and future service integration.

## Design science approach

The work follows the same evidence-led discipline I use across NamAir and NamMar while keeping the livestock domain and experience purpose-built:

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
- **Production claims stay controlled.** A working demonstration is not described as a certified veterinary, financial or regulatory system.

## Namibia-first details

The interface uses Namibian geography in sample records, NAD currency, Southern African date and time language, metric herd units and simple field vocabulary. It is designed for intermittent connectivity and phone-sized screens without assuming that every farm has continuous broadband or a dedicated data clerk.

The product starts with cattle operations in Namibia while leaving room for other herd types, regional practices, multiple properties and partner workflows after the correct domain and governance work is done.

## Engineering overview

- Responsive HTML, CSS and JavaScript working surface.
- Browser-local persistence for draft records and photo attachments.
- Zero-dependency Node HTTP API for controlled local demonstrations.
- Static Cloudflare-compatible build with private-by-default access.
- Accessible semantic navigation, keyboard-focusable records and readable status cues.
- JSON and CSV export, print-friendly layouts and clear sample-data labels.
- No client-side API keys, live weather claims or fabricated satellite/map values.
- Private source and deployment configuration intentionally separated from this public case study.

## Production path

The private test site is a controlled demonstration surface. A production rollout would add named accounts, farm tenancy isolation, MFA, owner/manager/field/vet roles, encrypted object storage for images, signed downloads, append-only audit history, conflict-safe offline sync, backup and restore drills, rate limits, secure headers, dependency scanning, monitoring, incident response and a Namibia-specific data-protection review.

Those controls are documented in the private build's hardening plan. They are prerequisites for accepting real farm records, not claims that a prototype has already satisfied them.

## Safety and data boundary

All names, tags, animals, dates, costs, camps, treatments and events shown in the demonstration are fictional onboarding data. Omutambo does not diagnose animals, prescribe treatment, approve sales, make financial decisions or replace a qualified veterinarian, owner or manager.

Live weather, map, satellite, market-price and external veterinary integrations are not implied by the demo. Any future provider must show source, timestamp, coverage and limitations at the point of use.

## Repository boundary

This public repository intentionally contains product narrative only. It excludes:

- deployable private application source and backend implementation;
- credentials, API keys, tokens and environment variables;
- customer, pilot, owner or livestock records;
- animal photos and private exports;
- database schemas, migrations and internal endpoints;
- private deployment identifiers and operational runbooks.

Please report security concerns privately to [freeman.ipumbu@outlook.com](mailto:freeman.ipumbu@outlook.com), not through a public issue.

---

© 2026 Freeman Ipumbu. Shared for portfolio evaluation and product discussion. No licence is granted to reproduce the product, branding or documentation.
