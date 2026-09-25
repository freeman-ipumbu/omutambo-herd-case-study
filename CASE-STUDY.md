# Omutambo Herd Operations — case study

Omutambo joins tagged livestock, poultry operations, photographs, health and breeding records, camps, movements, tasks and NAD costs into one farm workspace. The interface uses actual register totals and explicitly separates fictional demonstration records from the owner's live farm.

The deployed owner release persists versioned records in Cloudflare D1, checks signed identity at the API, preserves conflicting drafts, and supports complete JSON backups. The deployed access-management release adds named invitations, single-use activation codes, expiring permissions, owner revocation and access history. Each tester operates in a separate demonstration workspace.

The production build covers cattle, goats, sheep and freely named livestock species plus flock-level poultry inventory, production, feed, mortality, health and biosecurity records. Its remaining authenticated owner smoke check is recorded explicitly in the release status.

<!-- RELEASE-STATUS:START -->
## Release status

**livestock-poultry-1 — Multi-species livestock and poultry operations deployed; authenticated owner smoke check pending.**

Current deployed system: Production now includes cattle, goats, sheep and freely named livestock species plus flock-level poultry inventory, eggs, feed, mortality, weight, health, movement, cleaning, water and biosecurity records; the public front page remains at https://omutambo.pages.dev with protected sign-in and the existing verified invitation boundary.

Review scope: Invitation-only test programme; each tester has a separate demo workspace; only the owner can access live farm records.

Verification: **100 automated checks passed** in the released application build. These cover record handling, multi-species migration, poultry inventory and operating measures, signed identity, invitation activation and replay, expiry, revocation, role boundaries, isolated workspaces, backups and browser-draft behaviour. The production deployment and anonymous Access boundary were checked after upload. Earlier hosted drills verified owner administration, invitation creation/revocation, photograph save/reload, backup export, second-email activation, isolated demo saving, viewer restrictions, consumed-code rejection and existing-session revocation.

Operating limits: 10 MiB per workspace including photographs; latest 20 saved revisions; up to 200 access records.

Remaining launch gates:

- Run the post-deployment owner save, reload, export and restore smoke check through the email-authenticated production session; keep live farm records unchanged.
<!-- RELEASE-STATUS:END -->

## Design and responsibility

Freeman Ipumbu: product strategy, research, interface design and systems engineering. The work carries forward NamAir and NamMar principles of visible state, explicit freshness and human authority through a multi-species farm record model.

The refreshed visual identity is built around a kraal opening into a field path, with one center point for the animal or record under care. The shared vector mark now connects the public front door, protected workspace, owner console, browser icon, installable-app manifest and social preview as one product system.

Demonstration examples are fictional. This product records operational decisions; it does not diagnose animals, prescribe treatments, approve sales or replace a qualified veterinarian. The test programme is not a claim of full commercial farm tenancy, regulatory certification or unlimited image storage.

The public repository contains the public website assets and case study. Private source, records, credentials and deployment configuration remain separate.
