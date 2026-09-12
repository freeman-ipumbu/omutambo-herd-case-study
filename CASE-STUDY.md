# Omutambo Herd Operations — case study

Omutambo joins tagged cattle, photographs, health and breeding records, camps, movements, tasks and NAD costs into one farm workspace. The interface uses actual register totals and explicitly separates fictional demonstration records from the owner's live farm.

The deployed owner release persists versioned records in Cloudflare D1, checks signed identity at the API, preserves conflicting drafts, and supports complete JSON backups. The deployed access-management release adds named invitations, single-use activation codes, expiring permissions, owner revocation and access history. Each tester operates in a separate demonstration workspace.

<!-- RELEASE-STATUS:START -->
## Release status

**public-launch-1 — Public website live; owner-managed invitation access enabled and verified.**

Current deployed system: Public front page at https://omutambo.pages.dev with protected sign-in; hosted second-email identity verification, invitation activation, isolated demo save, viewer restriction, activation replay rejection and existing-session revocation verified; owner administration, photographs and backup export verified.

Review scope: Invitation-only test programme; each tester has a separate demo workspace; only the owner can access live farm records.

Verification: **88 automated checks passed** in the released application build. These cover record handling, signed identity, invitation activation and replay, expiry, revocation, role boundaries, isolated workspaces, backups and browser-draft behaviour. Local browser review also exercised the owner invitation form. Hosted owner administration, invitation creation/revocation, photograph save/reload and backup export have also been verified. Hosted second-email activation, isolated demo saving, viewer restrictions, consumed-code rejection and existing-session revocation have also passed.

Operating limits: 10 MiB per workspace including photographs; latest 20 saved revisions; up to 200 access records.

Public website: https://omutambo.pages.dev. The owner controls invitation access through the hosted administration console.
<!-- RELEASE-STATUS:END -->

## Design and responsibility

Freeman Ipumbu: product strategy, research, interface design and systems engineering. The work carries forward NamAir and NamMar principles of visible state, explicit freshness and human authority while using a cattle-specific record model.

Demonstration examples are fictional. This product records operational decisions; it does not diagnose animals, prescribe treatments, approve sales or replace a qualified veterinarian. The test programme is not a claim of full commercial farm tenancy, regulatory certification or unlimited image storage.

The public repository contains the public website assets and case study. Private source, records, credentials and deployment configuration remain separate.
