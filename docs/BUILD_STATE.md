# UrologAI Content build state

## Identity

| Field | Value |
|---|---|
| Product | UrologAI — The Living Urology Encyclopedia |
| Repository | `urologai/urologai-content` |
| Visibility | public |
| Default branch | `main` |
| Role | Sanitized public release projection only |
| Public hostname | `urologai.org` |
| API hostname | `api.urologai.org` |
| Staff hostname | `staff.urologai.org` |

## Plan and decision pins

- Build plan: v1.1, normalized SHA-256 `8f0e3fd8d30302fc7714f9ab7aa204cb814e7fda36edf54faeee7e018492f1fc`.
- D01: UrologAI naming, the `urologai` organization, three-repository topology, domains, and neutral independent identity are accepted.
- ADR-WORK-001: initial background work uses claimed Codex/Claude Code batches and immutable build/Render receipts; only gated sanitized projections enter this repository.
- PLAN-001: interactive corpus generation uses user-selected allowance envelopes, one independently committable batch at a time, and a `paused_budget` safe stop.
- ADR-WORK-002: agents may not spend below the reserve floor, automatically buy credits, redeem resets, or switch to API billing.
- Historical plan references to `urowiki-content` resolve to this repository.

## Block ledger

| Block | Status | Outcome | Evidence | Next permitted block |
|---|---|---|---|---|
| `B01` | bootstrap complete | Establish the repository with one governance-only initial commit | Root B01 handoff manifest pins this commit | A later named content block after its dependencies |
| `PLAN-001` | complete | Add credit-budgeted, resumable corpus batches without changing frozen plan v1.1 | `docs/build-history/20260919T194616Z-PLAN-001-codex.json` pins implementation `f621d491223ad358dbcd0e50600b89c6eaa43977` | A later named content block after its dependencies |

The immutable initial commit SHA, numeric GitHub repository ID, node ID, and remote settings are recorded outside this self-referential commit in the B01 root handoff manifest.

## Initial control state

- Rulesets and branch protection: none at B01; later named provisioning blocks establish them.
- License: intentionally unresolved; no license file is present.
- Clinical content, seed drafts, source copies, private data, implementation code, workflows, secrets, donor source, DNS changes, and deployments: absent.
- Render target: not configured for this repository; material builds must still write a receipt recording `not_configured` until that changes.
- The legacy `jfantus/urowiki` prototype and `nocluetoday/OR_Prep` are outside this repository and remain unmodified.
