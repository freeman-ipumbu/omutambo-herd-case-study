# Omutambo Herd Operations — case study

Omutambo joins tagged cattle, photographs, health and breeding records, camps, movements, tasks and NAD costs into one farm workspace. The interface uses actual register totals and explicitly separates fictional demonstration records from the owner's live farm.

The deployed owner release persists versioned records in Cloudflare D1, checks signed identity at the API, preserves conflicting drafts, and supports complete JSON backups. The deployed access-management release adds named invitations, single-use activation codes, expiring permissions, owner revocation and access history. Each tester operates in a separate demonstration workspace.

<!-- RELEASE-STATUS:START -->
## Release status

**access-review-1 — Deployed for owner use; external tester activation awaits hosted identity verification.**

Current deployed system: Owner console, invitation creation and revocation, persistent access history, photo upload/save/reload, photo-inclusive backup export, and separate empty live farm verified on Cloudflare.

Review scope: Invitation-only test programme; each tester has a separate demo workspace; only the owner can access live farm records.

Verification: **88 automated checks passed** in the released application build. These cover record handling, signed identity, invitation activation and replay, expiry, revocation, role boundaries, isolated workspaces, backups and browser-draft behaviour. Local browser review also exercised the owner invitation form. Hosted owner administration, invitation creation/revocation, photograph save/reload and backup export have also been verified. The remaining hosted identity gates are listed below.

Operating limits: 10 MiB per workspace including photographs; latest 20 saved revisions; up to 200 access records.

Remaining external tester launch gates:

- Provide an owner-controlled tester email and complete the hosted email identity, activation, replay, isolation, viewer, expiry and existing-session revocation checks
- Enable the production email identity gateway for invited testers after the hosted authorization checks; preview access stays owner-only
<!-- RELEASE-STATUS:END -->

## Design and responsibility

Freeman Ipumbu: product strategy, research, interface design and systems engineering. The work carries forward NamAir and NamMar principles of visible state, explicit freshness and human authority while using a cattle-specific record model.

Demonstration examples are fictional. This product records operational decisions; it does not diagnose animals, prescribe treatments, approve sales or replace a qualified veterinarian. The test programme is not a claim of full commercial farm tenancy, regulatory certification or unlimited image storage.

The public repository contains narrative only. Private source, records, credentials and deployment configuration remain separate.
