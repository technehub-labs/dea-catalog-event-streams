# Change Requests: dea-catalog-event-streams

This index tracks every change request that lands on this repository.

| CR | Title | Status | Notes |
|----|-------|--------|-------|
| [CR-CR-EVT-CAT-04](CR-CR-EVT-CAT-04-catalogue-foundation.md) | Catalogue foundation (kit bring-up) | Landed (this PR) | Standard kit: pointer, dependencies, schema projection, gates 1-6, workflows, FOUNDATIONS, record standard. No records admitted. |
| CR-CR-EVT-CAT-02 | Initial population | Planned | Evidence-gated seed population per FOUNDATIONS §7. |

## Numbering

Series tag `CR-EVT-CAT-NN`, sequential. Cross-repo CRs that touch this
repository are recorded here with their home-repo identifier.
| [CR-EVT-CAT-02](CR-EVT-CAT-02-evt-cat-02.md) | Entity Ingestion Groundwork (candidate intake queue + gates) | **Proposed (this PR)** | Gated intake: queue + blocking queue gate + admission tool (candidate-state subtrees, content-derived ids); pin v2.6.0→v2.8.0 + shard-aware toolchain re-vendor. No records. |
| [CR-EVT-CAT-03](CR-EVT-CAT-03-evt-cat-03.md) | Event Candidate Corpus | **Landed (this PR)** | 825 queue submissions from 1 bank(s); manifest with sha256s; queue gate CONFORMANT; no entities change. |
| [CR-EVT-CAT-04](CR-EVT-CAT-04-evt-cat-01.md) | Event Candidate Admission Batch 02 (Adyen event: AUTHORISATION_ADJUSTMENT … Zoom event: webinar.updated) | **Landed (this PR)** | Admitted 825 `Event` CANDIDATE records via the gated intake workflow (queue gate → admission tool → catalog gates); candidates +825, canonical unchanged; records at `lifecycle_status: proposed` in `candidates/` subtrees. |
| [CR-EVT-CAT-05](CR-EVT-CAT-05-cr-evt-cat-05.md) | CR Naming/Numbering Correction | **Landed (this PR)** | Programme batch CRs renamed to house-form CR-prefixed identifiers (mapping in the CR); content unchanged. |
| [CR-EVT-CAT-06](CR-EVT-CAT-06-cr-evt-cat-06.md) | Event Candidate Corpus Supplement (+201) | **Landed (this PR)** | 201 supplement submissions (extended vendor families); total queued 1,026. |
| [CR-EVT-CAT-07](CR-EVT-CAT-07-cr-evt-cat-07.md) | Event Candidate Admission Batch 02 (supplement) (Bitbucket event: issue:comment_created … Vercel event: project.removed) | **Landed (this PR)** | Admitted 201 `Event` CANDIDATE records via the gated intake workflow (queue gate → admission tool → catalog gates); candidates +201, canonical unchanged; records at `lifecycle_status: proposed` in `candidates/` subtrees. |
