<!-- chrono-instructions:begin -->
Registered rules; AGENTS.md is a literal relative symlink to CLAUDE.md.
Edit the listed catalog/file sources/manifest; run `chrono-instructions generate --host-root <host-root>`. Do not edit this block; the host owns exterior text.
Read host_context (may be empty) before work; do not reread these rules. Generation proves no AI reading/compliance or check execution.

<!-- Instructions modified, generalized and translated from Copyright 2026 The Omega Institute, Apache-2.0. License/provenance: optional legal reading, not policy. -->

manifest: `.chrono-harness/instructions/manifest.json`
catalog: `.chrono-harness/instructions/catalog.json`
host_context: `.chrono-harness/instructions/host-context.md`

# Requirement

Clarify requirements. Check the user’s goal, scope, constraints, real consumer and observable acceptance against the current SPEC. Follow requirement → audit → refactor → develop; verify consumption, then revisit SPEC. Consider the affected relationships before choosing the smallest sufficient change.

Work autonomously. Trust users, collaborators and AI as nonmalicious but fallible. Within authorization, implement, repair, migrate, validate and deliver, fixing rules/tools too; add no human approval, sign-off or stepwise confirmation gates.

Protect existing work. Use authorized isolated workspaces. For dev, create feature/integration from latest dev; check stability/rule/gate edits in fresh integration first. Pin baseline and net changes; moving checkouts give no fixed evidence. Immediately before authorized deletion, recheck target identity, locks and declared eligibility.

# Audit

Audit before extending. Compare requirements, current SPEC, real consumers, existing capabilities and retained evidence; check ownership, explicitly registered dependency impact and validation, CI and storage costs. Search the repo, pinned direct dependencies and allowed external sources, including private definitions and valid failure findings; verify interfaces, assumptions and scope. Reuse sufficient capability. Invisible is not absent; global consideration does not require a whole-repo audit or test run for every change.

Use explicit allowlists. In host .chrono-harness/ FILEMAP or registry, list file owners, inputs, consumers, dependencies, costs and operations; mark unknown costs unknown, not zero. AI may maintain it autonomously. Executors consume declarations, never infer tests from directories, languages, names, scans, reflection, calls or IO. Diagnose/fix omissions, ambiguity and missing inputs; no all-check fallback, guessed dependencies or false no-work.

Inspect failures first. On failure, timeout or no result, read available authorized errors, inputs, outputs, exits and logs before diagnosis/repair. Verify input matches dispatch intent. Silence, low CPU, missing output or timeout alone proves neither inactivity, a hang nor difficulty. Without evidence, leave causes unverified.

Improve using measured costs. Check input size, dependency scope and build, validation, CI and storage costs; report method, units, window and comparison basis, leaving unknowns explicit. Remove waste, poor representations and duplicate dependencies, then remeasure and verify real host consumption. Do not buy success with higher budgets, repeated runs, deleted necessary tests or weaker goals.

# Refactor

Refactor at the natural owner. Give definitions, state, outputs and operations one authority and actual producer. When audit establishes an ownership or coupling problem, refactor there and remove verified redundancy before extending; require no refactor without a problem. Keep local understanding to the unit’s inputs, interfaces and explicit dependencies. Register links/aliases to real sources; history belongs in version control, and narrative/provenance cannot dictate dependencies or gain runtime authority.

Keep projects small and independent. Build production projects independently unless they must build together; each has a dedicated test project checking real code via explicit dependencies. No recursive test projects. Standalone scripts/tests may register separately; no empty projects, umbrella builds or splitting shells.

# Develop

Develop real gaps. When existing capability is insufficient, bind development to a real consumer and acceptance; create no empty calls, duplicate platforms or speculative extension layers. Separate common product behavior from host policy. Hosts explicitly register replaceable scripts, plugins, judges and config under .chrono-harness/; do not hardcode host instances or edit global config.

One current registered entry per activity. Each governed build, generation, check and delivery follows its current canonical route. Choose customization in registration before execution; ordinary instructions expose that route without parallel recipes. Declare parameters, prerequisites, inputs, environment, outputs and exits. Change a method through registration and applicable verification, retaining one formal entry. Delegate within layers to existing code, without copied recipes; fix the error-producing layer.

Register judges first. Assign applicable machine-checkable default/project rules to explicit configurable judges. Register methods, decision rules and required inputs before acting. Run designated judge binaries; deviations from registered methods/rules are errors.

Revise rules autonomously. Try existing rules first. Explain why judges/policies change, their impact and check costs; finish applicable checks/migration. Broader impact needs broader checks; self-checks and reviews prove no absolute correctness.

Disclose mixed policy/product changes. List both changes, old/new effects and check costs; warn visibly and finish all applicable checks. No human gate or forced separation, no excused failures or independent self-review assurance.

## Verification and SPEC iteration

Judge DELTA only. Select checks by the impact closure of changes and explicit dependencies at both ends, including deletions, renames and registry-edge changes. Trace failures to changes/dependencies; fix omissions, no full-repo fallback. Complete inputs and local judgments are prerequisites; graph closure proves no semantic completeness.

Run candidates, read baselines. Pin candidate and eligible baseline identities. Run only tested candidate judges; other revisions are fixed data in declared roles. Never run past judges or read moving latest branches during judgment. Immutable OIDs fix bytes, not eligibility or semantic truth.

Match local/CI inputs. Use one registered check command. Equal verdicts require identical effective inputs, scope, policy, executables, toolchain and environment, plus determinism. Local feedback, shallow checks or static shape cannot replace remote tests. Diagnose differences; local green alone cannot explain remote red.

Test behavior. For critical parsing, judgment or state logic, predefine independent success/failure/boundary expectations; where feasible, see pre-change failure, then implement and pass. Use mutation to verify detection when needed. No shape tests duplicating reversible prose/pure forwarding; scripts’ critical logic still needs testing.

Test in the implementation language. Each independent unit uses its implementation language for tests, assertions, drivers and test subprocesses; sh/bash may use Python tests. Do not hide foreign-language test logic in embedded scripts, interpreter arguments or thin wrappers. Keep genuine external-interface fixtures in separately registered files. Register pairs per unit in mixed-language hosts; do not infer languages, directories or dependencies.

Programs produce their state. Active producers generate program success, failure and domain state; never hand-fill success. Unrun checks give no assurance. Shallow checks, wrapper exits or workflow steps prove no unvalidated results.

## Delivery and cleanup

Verify delivery. For merges/releases, verify state, landed SHA, artifacts and required post-landing checks. Commits, open PRs, green checks or CLOSED alone prove no delivery. Explain tested/landed tree differences; validate affected scope. For caller-owned lifecycles, state handoff; this stage is not delivery.

Keep useful artifacts. Place code, current specs, needed experiments/data, sources, licenses and necessary program-maintained state properly. Search/enumeration/counterexample/boundary experiments stay useful without prose citations or main-build inclusion. Preserve reusable failure criteria or regressions.

Clean promptly and preserve work. Use the host’s registered lifecycle entry to protect consumption, join all owned/background jobs, verify completion/landing and hand off. Adopted and verified automatic recovery/cleanup paths reclaim reproducible output after interrupted sessions promptly; do not rely only on remembering finish. Cache disposal never claims completion. Before deletion, check actual ownership, active use, required consumers and retention conditions; preserve source, unretained commits, needed evidence and original failures. Age, directory names and idle time prove no disposal eligibility. Host context and the lifecycle owner define operations, compatible rollout and recovery limits.
<!-- chrono-instructions:end -->
