# W00 — A00 implementation review

**Decision: CHANGES REQUIRED.** A00 supplies a substantial executable foundation. Correct W00-F07 and place the approved master at its required repository path before accepting the shared base for A01/B00. This is a bounded A00 correction; later application features are not prerequisites for accepting the scaffold.

**Reviewed:** 2026-09-16. Implementation `605a73f4feaf245c2eabc82d6701ef13b6e1efe6`; submission head `4e3494db5502af821c7706cd831ace38b02e82c4`; human merge [PR #3](https://github.com/Nakum-hub/Cyberfyx-ORVIA/pull/3) at **`e839b1a0e9358d389c5cb728648b1590f8f7ef9e`**. Submission and merged tree are identical: `1c09d4b6c48c51cb907797d692cd50ec61c50f7d`. Contract proposal **0.2.0**, plan 1.0, master document revision 1.3, CUSTOMER_LOCAL_SYNTHETIC. Work performed no merge.

## Architecture, contract and ownership conclusions

Keep ADR-001's selected stack and marketing-withdrawal scope. A00 preserved the existing planning files and added its scaffold. Inventory, pinned dependencies, migration, persistent Temporal probe, generated interfaces, isolated profiles and explicit UI handoff now exist. No framework rewrite or AI/vendor runtime is justified.

The proposed command envelope explicitly binds installation, tenant/legal entity/environment, workflow/action, capability/version, schema version, exact scope/plan/approval digests, expiry, nonce and operation budget. Independent-review or explicit policy-authorised non-destructive approval outcomes are represented. The signing helper is not agent enrolment, replay persistence or current-authority enforcement; those remain A03/A06.

Immutable receipt replay versus GET current projection, scoped idempotency ordering and separate reconciliation records address the earlier missing definitions. Unknown attempts remain historical facts. Environment-scoped purposes retain the master's four-part consent aggregate. Distinct staff/principal/machine mounts and rejection of ambiguous dual staff/principal sessions are acceptable prototype rules. Actual identities, MFA, transactions and denials remain A01/A02.

The progress validator permits legitimate progress and rejects invalid dependencies, missing evidence, view drift and fabricated application PASS from a bootstrap subset. Keep canonical JSON ownership and the task graph. The generated seed is an explicitly new proposal, not a recovered original; Codex remains its writer. Do not import an older seed.

The transfer of `apps/web/src/app/layout.tsx` and `page.tsx` to Claude Code is explicitly conditional on shared-base acceptance. Codex retains API/server/auth, health route, configuration, dependencies and schemas. B00 must consume generated clients/auth bindings, confirm the contract handoff and use isolated profile `ui-b00`. Separate worktrees alone do not isolate credentials, ports, databases, volumes, Temporal state or artifacts.

## Actual execution and evidence limits

Work installed selected Node **24.21.0**, pnpm **12.4.2** and the unchanged frozen lockfile in the isolated review checkout. Transient dependency-download tunnel failures recovered normally; engine/peer/age/build-approval safeguards were not disabled.

All evidence below is under `docs/reviews/work/artifacts/W00-A00-e839b1a/` unless linked elsewhere.

| Executed check | Result | Record |
|---|---|---|
| Frozen install | PASS, exit 0 | `frozen-install.json` |
| Existing contract/domain/client/tracker unit suite | 8 PASS, exit 0 | `unit-loader.json` |
| Generated contract drift/examples | PASS: 8 artifacts, 37 routes, 7 error examples | `contracts-loader.json` |
| Typecheck / lint | PASS / PASS | `typecheck.json`, `lint.json` |
| Tracker/views and tracker tests | PASS: 23 tasks, 34 definitions, 3 tests | `tracking-check.json`, `tracking-unit.json` |
| Provider assertion under observation completion criterion | FAIL, exit 1; actual COMPLETED, expected NEEDS_ATTENTION | `F07-counterexample.json`; [reproducer](repro/W00-F07-provider-receipt.mjs) |
| Counterexample controls | ACK alone, fresh scoped read, stale scoped read all behave as expected | Same report, three passing controls |
| Generated payload hashes / submission versus merge tree | 7 hashes match; trees identical | `source-and-evidence-audit.json` |
| Source whitespace / narrow local hygiene | PASS / PASS | `source-whitespace.json`, `local-hygiene.json` |

Ordinary `pnpm test` and `contracts:check` failed here because the tsx CLI's IPC listener was denied with EPERM. Those failures remain in `unit.json` and `contracts.json`. The same unmodified tests/generator passed using pinned Node with `--import tsx`, without a CLI listener. This does not claim the original CLI entry points passed. Initial dependency-free tracker checks used preinstalled Node 24.19.0; subsequent unit/contract/type/lint checks used 24.21.0.

Work reviewed **51** Codex command reports, including **14** retained nonzero runs. The latest build's recorded source hashes match the merged files. Final unit/type/contract-check snapshots differ only in two later-edited engineering documents. Codex recorded dirty pre-commit source at `e5cdef3`; those are not relabelled as executions on `e839b1a`. The per-file audit records actual differences, including older service/reset snapshots. Generated-manifest verification alone is not regeneration; both checks were executed separately.

Codex's retained logs support PostgreSQL write/read, Temporal execution and restart persistence, OPA positive/negative readiness, bootstrap reset and built HTTP smoke at **bootstrap depth**. Work has no Docker/PowerShell and did not independently rerun those services, Windows setup, Next build, browser/application acceptance, egress capture, recovery or rehearsals. Advisory/security qualification remains unexecuted. Full prototype T01–T34 remain NOT_RUN; partial bootstrap evidence and the pure-domain failure do not become full-scenario PASS or FAIL.

## Findings and retests

### W00-F07 — High — provider assertion satisfies the independent-observation criterion

- **Task/files/candidate:** A00, then A03/A05 consumers; `packages/domain/src/completion.ts:5–8`, `packages/contracts/src/index.ts` Observation/Obligation; `e839b1a0e9358d389c5cb728648b1590f8f7ef9e`.
- **Reproduction/evidence:** after frozen install, run `node docs/reviews/work/repro/W00-F07-provider-receipt.mjs` using Node 24.21.0. A required CURRENT_SCOPED_OBSERVATION obligation, ACKNOWLEDGED execution and fresh PROVIDER_RECEIPT asserting restriction return COMPLETED with no independent target read. The helper accepts every method except NONE. Exit 1 and exact expected/actual values are retained; the existing eight tests miss this case.
- **Expected:** a provider receipt remains an attributable assertion and cannot satisfy this independent scoped-observation criterion. Master §44 separates provider assertions and independent observation. A fresh matching scoped read may satisfy it; stale/missing observations may not. Reconciliation retains unknown/ACK history.
- **Owner/correction:** **Codex** corrects the predicate and necessary canonical refinements, adds the regression and regenerates versioned artifacts together. Retain provider receipts as evidence/reconciliation input. Do not remove the criterion, rewrite history or broaden scope. Work reviews semantics; Claude Code consumes the coordinated contract revision.
- **Retest:** the supplied counterexample must return NEEDS_ATTENTION for provider-only evidence, retaining all three controls. Run existing contract/domain tests, generated drift and typecheck on the fix SHA. A05/B03 and later T18/T21/T29 must preserve provider/manual/independent-observation distinctions. Those later features are not required for this predicate fix.

### W00-F01 — High — remaining source-provenance gate

- **Task/file/candidate:** W00/A00; `docs/source/ORVIA_Version_1_Unified_Master_with_Version_2_AI_Roadmap.md` remains absent at `e839b1a`.
- **Evidence:** exact inventory and source audit. Work and Codex independently hash the supplied original to `527daa1d6a2a7564a61d0375e540ca66b1bc8f33f4e71d327b0f6cb0bf6dbef6`. Earlier missing scaffold/inventory/handoff portions of F01 are resolved.
- **Expected/owner:** **human** commits the already approved, unmodified original at that human-controlled path. Work has the reference; another upload or production secret is unnecessary.
- **Retest:** recompute SHA-256 on the committed repository copy, compare to the approved original and record its commit. Review any actual source difference before acceptance.

| Earlier finding | Disposition / retained gate |
|---|---|
| F02 command bindings | Resolved at contract/helper depth; real agent scope/replay/current-generation denials remain A03/A06 T12. |
| F03 reconciliation/receipt | Definitions/examples resolved at A00 depth; F07 blocks completion semantics. Transactional/race/failure tests stay A02–A06. |
| F04 progress validator | Resolved through source review and independent execution; canonical ownership stays Work. |
| F05 environment/timing | Windows resources/profiles/preflight supplied. Actual R0/deadline remains unknown and does not block bootstrap; no restarted clock. |
| F06 publication access | Previously resolved. No new access installation or permission request. |

## Retained later-ticket gates

| Owner / review | Evidence still required at the assigned stage |
|---|---|
| A01/A02, W01 | Real staff/principal/MFA authority; least-privilege non-owner database roles/RLS and tenant-aware references; sibling tenant/environment denial; independent exact-version approval; auth before receipt replay; atomic consent/event/outbox/idempotency; stale grants, concurrent epochs and fresh re-consent. |
| A03/A04, W02 | Agent independently checks signed/current authority, capability, nonce/budget and epoch/generation; target mutation enforces freshness. Actual send admission shares ordering with withdrawal; preview ALLOW has no authority. Order-service has a separate condition; OPA failure is closed. |
| A05/A06/B03/B04, W02 | Applied timeout reconciles safely before retry; ACK-without-effect, permission loss, manual work and stale observations remain distinct; bounded retries, truthful counts/local scoped exports, healthy/broken regression. |
| A06/A07 | Target-only restore stays quarantined against the current ledger. Full reset needs a durable admission/drain guard, not only a point-in-time Temporal listing. A00 deletes only bootstrap probes and refuses later business tables; it does not qualify full application reset. |
| A06, W02/W03 | Measure runtime egress with vendor/model routes blocked. The fixed relay has an external-capable bridge and is not proof of a firewall. Setup downloads do not establish runtime egress. Verify local assets/telemetry and candidate exposed-path TLS. |
| A07/B06/C02, W03 | Exact frozen integrated build, complete P0 and any promoted P1, reproducible package, truthful capability/runbook claims and two rehearsals. Production security/legal gates remain separate. |

## Next integration action

1. Codex submits the bounded A00 F07 correction and retest artifacts. Human supplies the master path. **Cowork C00** can proceed independently now.
2. Work reviews that exact SHA and records W00/A00 acceptance if blockers close; human approves integration. PR #3 being merged does not imply a passing review.
3. Then **A01 and B00** are ready to start; W01 can begin review. B00 acceptance also needs C00. Confirm its conditional UI transfer and use `ui-b00`.
4. Preserve A01 → A02 → A03 → A04/A05 → A06. Codex remains one writer; A04/A05 need not run concurrently. A07 starts after A06 and is accepted only after W02; W02 also needs W01/B04 evidence. B06/C02 and W03 follow their recorded gates. No blanket approval to start/accept all A01–A07 together.

W01/W02/W03 reports will review actual dependencies; empty report files are not completed reviews. Retain R14–R20 rest/handoff, R28 freeze and test/rehearsal reserve without inventing a deadline or resetting the 36-hour budget. No recurring scheduling, automatic cross-tool orchestration, deployment or release is created.
