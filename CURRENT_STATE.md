# ORVIA — current execution state

**Writer:** Work · **Checkpoint:** W00/A00-review-r3 · **Date:** 2026-09-16

| Field | Current evidence / decision |
|---|---|
| Inspected integration | main at e839b1a0e9358d389c5cb728648b1590f8f7ef9e; human merged A00 PR #3 at 09:42:57 UTC |
| A00 submission / tree | Head 4e3494db5502af821c7706cd831ace38b02e82c4; implementation 605a73f4feaf245c2eabc82d6701ef13b6e1efe6; submission and merge tree identical: 1c09d4b6c48c51cb907797d692cd50ec61c50f7d |
| Work proposal | prototype/work/W00-a00-review, based on inspected integration; publication commit identified by its Git/PR record. Work has not merged it |
| Source | Product V1, master revision 1.3; reference SHA-256 527daa1d6a2a7564a61d0375e540ca66b1bc8f33f4e71d327b0f6cb0bf6dbef6 reverified; required human-controlled repository copy still absent |
| Plan / contract | Plan 1.0; design 0.1.0; executable proposal 0.2.0 reviewed, freeze held for F07 correction |
| Profile / scope | CUSTOMER_LOCAL_SYNTHETIC marketing withdrawal; existing stack retained; custom AI DEFERRED_V2; no P1 promoted |
| Owners | Work: decisions/reviews/canonical trackers/views/state/common template. Codex: schemas/dependencies/core/infra/tests. Claude Code: UI/browser after accepted A00 transfer. Cowork: UX/capability/demo/runbooks. Human: source/access/system approvals/merges/release |
| Accepted tasks | W00/A00 acceptance remains blocked. Merged code and reviewed evidence do not imply task acceptance. A01–A07/B00 are not accepted |
| Work execution | Pinned frozen install, 8 existing unit tests, typecheck, lint, generated contracts/examples, trackers, hash/whitespace and narrow hygiene checks pass. F07 counterexample fails: provider assertion alone yields COMPLETED. CLI IPC failures and loader reruns retained |
| Producer evidence | 51 recorded commands, including 14 nonzero runs; source hashes reviewed. Windows service/start/reset/HTTP evidence supports bootstrap subsets only. Work did not rerun Docker/PowerShell/services/browser here |
| Full application results | T01–T34 all NOT_RUN: 30 P0 and 4 unpromoted P1. Partial bootstrap and pure-domain checks linked without promoting full-scenario results |
| Blockers | F07 High: provider receipt satisfies independent-observation completion criterion (Codex). F01 remaining source gate: approved master absent under docs/source (human) |
| Resolved / deferred | F02 bindings and F04 validator resolved at A00 depth; F03 representation supplied but F07 blocks completion semantics. F05 runtime supplied; R0/deadline unknown, nonblocking. F06 publication access resolved |
| Isolation | Producer measured codex-a00; ui-b00/rehearsal unmeasured. Work used static/unit review with no services. Full reset, TLS and egress remain later gates |
| Readiness | Shared-base CHANGES_REQUIRED; internal demo NOT_READY; production security/legal/release NOT_ASSESSED |
| Next ready work | Codex A00 F07 correction; human source placement; Cowork C00 independent. A01/B00 start after accepted corrected A00; B00 acceptance also requires C00 |
| Next merge | Human reviews this Work checkpoint, then corrected A00/source commits and relevant retests. Only human approves integration/release; Work re-reviews the exact correction |

| Work ticket | Status | Dependency / deliverable |
|---|---|---|
| W00 | BLOCKED for acceptance; concrete implementation review delivered | [A00 review](docs/reviews/work/W00_A00_REVIEW.md), ADR-001, evidence and [handoff](handoffs/work/W00-e839b1a.md); retest F07/source |
| W01 | NOT_STARTED | Start accepted A00; accept A01/A02; authority/consent review |
| W02 | NOT_STARTED | Start W01/A03; accept A04/A05/A06/B04; failure/security/recovery review |
| W03 | NOT_STARTED | Start W02; accept A07/B06/C02; exact candidate, required evidence and two rehearsals |

Work alone consolidates this table. Other lanes submit factual handoffs. Canonical definitions remain tracking/tasks.json and tracking/acceptance.json; generated views match. Accepted commit fields remain null until acceptance. Preserve failures/retests against their original source identity. Actual R0/deadline is still requested; the original 36-hour budget has not restarted.
