# CR-EVT-CAT-06: Event Candidate Corpus Supplement (+201)

**Status**: Landed (this PR)
**Layer**: Catalog content (candidate corpus intake)
**Owner**: Emmanuel A. Otchere
**Date**: 2026-11-15
**Admission authority**: candidate corpus only (canonical admission remains the evidence-gated step; FOUNDATIONS D-4/D-5)
**Trigger**: Catalog population programme. The baseline corpus (CR-EVT-CAT-03, 825 records) fell short of the programme's 1,000-candidate minimum; this supplement adds 201 documented event types from additional vendor families (GitLab, Bitbucket, Mailgun, Postmark, Mailchimp, Discord, Salesforce Platform Events, Datadog, CloudEvents, Sentry, Confluence, Google Workspace, Vercel, Terraform Cloud) to reach 1,026.
**Carrier**: Single PR on feature branch `feat/cr-evt-cat-06`. PR review, not direct push.
**Depends on**: CR-EVT-CAT-02 (groundwork), CR-EVT-CAT-03 (baseline corpus), CR-EVT-CAT-04 (batch admission).

## 1. What this CR lands

**201 additional Event candidate submissions** in `contributions/queue/<shard>/` (gate-CONFORMANT; total queue now 1,026). Provenance: supplement bank sha256 recorded in `ingestion/manifest.yaml` (updated by this CR); per-record `published-document` citations to the vendor events documentation pages.

## 2. Verification

- `check_contributions.py`: CONFORMANT (1,026 queue files)
- No directory holds 800+ entries
- No `CATALOG.yaml` change (queue ≠ index)

## 3. NOT-List

- NOT record admission (follows in CR-EVT-CAT-07).
- NOT a modification of gates, schemas, or intake tooling.

## 4. Acceptance criteria

1. 201 supplement submissions gate-CONFORMANT; manifest updated.
2. Total queued = 1,026 (>= the 1,000 programme minimum).
