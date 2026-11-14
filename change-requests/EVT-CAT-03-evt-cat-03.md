# EVT-CAT-03: Event Candidate Corpus

**Status**: Landed (this PR)
**Layer**: Catalog content (candidate corpus intake)
**Owner**: Emmanuel A. Otchere
**Date**: 2026-11-15
**Admission authority**: candidate corpus only (canonical admission remains the evidence-gated step; FOUNDATIONS D-4/D-5)
**Trigger**: Catalog population programme (2026-11 owner directive): advance 10 foundational skeleton catalogs with evidence-backed candidate corpora (>=1,000 each) through a gated intake workflow. Event-streams is ninth: composed vendor event/webhook documentation catalogs (GitHub, Stripe, Slack, Shopify, cloud + SaaS vendors — each record is a documented vendor event type citing its published documentation page) are the candidate seed sources named per FOUNDATIONS §7.
**Carrier**: Single PR on feature branch `feat/evt-cat-03`. PR review, not direct push.
**Lands against**: `main`
**Depends on**: EVT-CAT-02 (ingestion groundwork).

## 1. What this CR lands

**825 Event candidate submissions** in `contributions/queue/<shard>/<slug>.yaml` from 1 evidence bank(s):

| Bank | Source | Records |
|---|---|---|
| vendor-catalogs.json | Composed vendor event/webhook documentation catalogs (GitHub, Stripe, Slack, Shopify, cloud + SaaS vendors) | 825 |

Provenance in `ingestion/manifest.yaml` (bank sha256s, source URLs, retrieval dates, mapping note). Every submission carries `source_ref`, a `published-document` evidence citation, and published description prose. Provisional field mappings are documented per record and in the manifest; per-organization values are canonical-admission decisions.

> Composition note: records encode documented vendor event types (verbatim identifiers from the vendor's published events documentation); stream bindings are provisional candidate values subject to canonical-admission review.

## 2. What changes

- `contributions/queue/<shard>/` — 825 intake submissions (`status: queued`)
- `ingestion/manifest.yaml` — corpus provenance record (new)
- No `CATALOG.yaml` change (queue ≠ index)
- This CR file and the index row

## 3. Verification

- `check_contributions.py`: CONFORMANT (825 queue files)
- No directory holds 800+ entries (slug-prefix distribution)
- Spot-checks: records trace to their published source identifiers

## 4. NOT-List

- NOT record admission (nothing under `entities/` changes; admission follows in EVT-CAT-04+).
- NOT a modification of gates, schemas, or intake tooling.
- NOT an authoritative assessment of provisional mapped values.

## 5. Acceptance criteria

1. 825 gate-CONFORMANT submissions; manifest carries bank sha256s + source URLs.
2. Submissions carry no `id`; `status: queued`; `submitted_by: Emmanuel A. Otchere`.
3. `CATALOG.yaml` counts unchanged.
