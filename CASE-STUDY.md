# Omutambo Herd Operations — public case study

Omutambo addresses a practical gap for Namibian cattle operations: records often live across notebooks, spreadsheets, WhatsApp messages and memory. The system creates one reviewable record for each animal and the work around it.

The experience borrows the strongest discipline from NamAir and NamMar: visible state, explicit freshness, explainable prompts, human authority and honest fallbacks. The domain model is purpose-built for cattle operations: tags, breed/sex/age, ownership, health treatments and vaccinations, breeding and calving, grazing camps, water points, movements, mortalities, sales and purchases, feed and veterinary costs, tasks, exports and print-friendly reports.

The private demo supports browser-local drafts, a zero-dependency local API, searchable cattle records, animal profiles, optional photo attachments, JSON/CSV export and print mode. Demo data is fictional and labelled clearly.

## Safety and boundary

Omutambo records decisions; it does not diagnose animals, prescribe treatment, approve a sale or replace a qualified vet, owner or manager. A production rollout requires authenticated farm tenancy, least-privilege roles, encrypted photo storage, audit history, conflict-safe sync, backups, monitoring and Namibia-specific data-protection review.

## Role

Product strategy, design research, systems engineering, interaction design, frontend/backend foundation, deployment shape and hardening plan by Freeman Ipumbu.
