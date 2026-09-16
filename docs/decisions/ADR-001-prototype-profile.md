# ADR-001 — Adopt the customer-local synthetic prototype profile

**Ticket:** W00 · **Revision:** repo-r3 · **Date:** 2026-09-16

**Decision owner:** Work · **Integration/release owner:** human

**Status:** Prototype profile adopted; actual A00 foundation preserved. W00/A00 acceptance remains blocked by F07 completion semantics and the required master copy under docs/source. A00 was human-merged in PR #3; merger alone is not acceptance. See [the implementation review](../reviews/work/W00_A00_REVIEW.md).

## Context and authority

The source is `ORVIA_Version_1_Unified_Master_with_Version_2_AI_Roadmap.md`, document revision 1.3, Product Version 1. Its complete reference-file bytes were obtained and SHA-256 independently recomputed:

`527daa1d6a2a7564a61d0375e540ca66b1bc8f33f4e71d327b0f6cb0bf6dbef6`

This matches the expected hash in the execution kit and project handoff. The current numbered sections and governing requirements control this decision; historical diff appendices do not supply alternate product requirements. No legal baseline or external technical-version claim was newly verified by this review.

The reviewed planning input is `ORVIA_Prototype_Execution_Kit_v1.zip`, plan 1.0, contract design 0.1.0. It contains the requested W00 assignment and matching role prompt. Its `docs/source/` contains only a README; the verified master was read separately. The earlier repository checkpoint inspected `Nakum-hub/Cyberfyx-ORVIA` at `96b8bd7590de0ca662d725b7fa0d708e811d6722`. That historical seven-file base contained only planning/instruction documents. The current A00 review inspects `e839b1a0e9358d389c5cb728648b1590f8f7ef9e`, whose tree equals submission head `4e3494db5502af821c7706cd831ace38b02e82c4`. It includes the actual scaffold, contracts, inventory and evidence; the master copy remains absent. Six governing documents were byte-identical to the agreed kit at that original planning base. The human-controlled master remains available as a separately verified reference; this Work branch does not change `docs/source/`. The older `ORVIA_36_Hour_Prototype_Build_Kit.zip` was not used as governing input.

## Decision

Adopt the existing plan's **CUSTOMER_LOCAL_SYNTHETIC** profile and marketing-withdrawal vertical slice. This is a bounded internal-demo addendum to the master, not a replacement product specification. Preserve compatible working code when A00 inventories the actual repository. No framework migration or rewrite is authorised by this ADR.

| Area | Adopted prototype decision | Source / limit |
|---|---|---|
| Runtime boundary | Workspace, Privacy Centre, API, policy service, databases, durable worker, agent, targets, logs and evidence remain local; local assets; no runtime vendor/model dependency | Master §§2, 11, 20, 31, 43, 63; prototype EXECUTION_PLAN §§2–4 |
| Slice | Authenticated grant/withdrawal, durable receipt and outbox, actual CRM restriction, independent observation, current send admission, uncertainty/manual gap, local evidence and real regression | Master §§16–18, 40, 44–47, 137, 191–194 |
| Targets | Synthetic CRM, ORVIA-built REST/send simulator and a declared no-API legacy target; two synthetic organisations and distinct principals | A simulator is not a supported commercial-vendor connector |
| Logical stack | TypeScript/Next, PostgreSQL, Drizzle, Better Auth, OPA, persistent Temporal development service and restricted local agent | Preserve compatible existing implementation. A00 supplies locked versions and Windows bootstrap service evidence; full application/resource qualification remains in later tickets |
| Packaging | One private local Compose profile; thin Next handlers call domain packages; shared application build with independently enforced staff/principal identities | Private synthetic adaptation only; public portal/private-admin production ingress is not qualified |
| Recovery | Worker recovery plus quarantined target-only synthetic restore against the current authoritative consent ledger | No claim of full control-plane restore, measured production RPO/RTO or enterprise disaster recovery |
| Security | Real authentication/MFA, scope checks, least privilege, protected bootstrap, signed restricted commands and current-authority checks remain P0 | No role switch, fake identity, arbitrary target or hidden fail-open substitute |
| Optional work | At most one explicitly promoted P1 slice after the core gate and test reserve permit it | No promotion or extra scope selected in W00 |
| Product AI | Custom models, embeddings, training, GPU work, model APIs and an AI-draft-import workbench remain excluded | Product Version 2 is preserved; company-authorised development AI is separate |

## Contract adoption boundary

Adopt the design's separated consent, workflow, action, observation, processing-decision and test-result axes. Accept durable withdrawal before propagation; ACK is not observation, a timeout is not proof of failure, and manual closure is not automated verification. Preview ALLOW never authorises later sending.

The master and prototype use different state vocabularies. Preserve the meaning rather than treating either vocabulary as permission to omit uncertainty:

| Master concept | Prototype mapping / freeze condition |
|---|---|
| §25 `OUTCOME_UNKNOWN` | Design `EFFECT_UNKNOWN`; retain the uncertain attempt and its evidence |
| §25 `RECONCILING` | 0.2.0 proposes separate PENDING → RECONCILING → terminal records linked to the immutable uncertain attempt |
| §44 acknowledgement | `ACKNOWLEDGED` is an execution fact, never an independent read |
| §44 observed verification | `OBSERVED_SATISFIED` is scoped, dated and limited; no unqualified universal VERIFIED label |
| §44 stale/missing observation | Preserve `STALE`, `UNVERIFIABLE`, `NOT_CHECKED` and unsatisfied observations as distinct facts |

**The contract is not yet frozen for implementation acceptance.** Executable proposal 0.2.0 resolves F02 bindings and the missing F03 receipt/reconciliation representation. Work executed its existing unit suite and generated drift check. W00-F07 demonstrates that a provider receipt can satisfy CURRENT_SCOPED_OBSERVATION; Codex must correct that predicate, preserve the separate evidence meaning and regenerate the coordinated contract revision. Existing A00 code stays in place. Work does not edit executable schemas or implementation.

Environment scope is also explicit: master §16 specifies the consent aggregate `(tenant, legal_entity, principal_reference, purpose)`. This review does not silently add an environment component or assume consent sharing. A00 documents that every prototype purpose belongs to one environment; composite authority/mapping checks must reject sibling-environment use. A01/A02 must implement and test those denials.

## Ownership and acceptance

Codex remains the sole schema/dependency/migration/server/worker/agent writer. Claude Code owns UI and browser tests after the recorded A00 layout transfer. Cowork owns UX, capability claims and operator/demo documents. Work owns decisions, its reviews, canonical task/acceptance tracking, generated views and consolidated state. The human owns access, system approval, integration and release. A00 records the conditional transfer of layout.tsx and page.tsx to Claude Code; it takes effect after shared-base acceptance. The common handoff template is restored unchanged from the matching kit under Work stewardship.

All 30 sprint P0 scenarios remain mandatory for completed internal-demo readiness. A partial demonstration must identify its passing slice and outstanding gates. Preserve the existing R14–R20 rest/handoff block, R28 freeze and final test/rehearsal reserve; actual R0 and the meeting deadline still require the human's timestamp. This does not block A00 inventory/bootstrap. The 36-hour budget has not restarted.

The full Version 1 supply-chain, supported-platform, recovery, legal and independent security gates remain separate, including master §§163–164. Neither this ADR, the planning validator nor a synthetic demo is production approval.

## Consequences and next dependency

This decision fixes the intended demo depth and boundaries while retaining all unrelated master requirements. Work changed no application implementation. Its independent checks cover existing unit/domain/client contracts, type/lint, generation and document consistency; F07 is an executed pure-domain failure. Producer service evidence is reviewed separately. Full application acceptance remains NOT_RUN; neither older document checks nor bootstrap probes establish it.

Next dependency-ready work is **the bounded Codex A00 F07 correction** and human source placement. Work retests the exact correction, then recommends acceptance/integration to the human. Keep the existing graph without a circular W00/A00 dependency. C00 is independent; A01/B00 and W01 wait for accepted A00. The original 36-hour budget, rest/handoff, freeze and test/rehearsal gates remain unchanged.
