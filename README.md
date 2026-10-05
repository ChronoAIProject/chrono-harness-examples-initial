# chrono-harness initial-host example

A documentation-only host demonstrating a historical first-root inventory and subsequent DELTA checks. Ordinary updates use public chrono-harness v0.1.0-beta.19. There are no production or test projects. All tracked files are explicitly registered; no project structure or language is inferred.

Install the pinned public release with `python3 .chrono-harness/install.py .`.
For the parentless root commit, run `.chrono-harness/bin/chrono-harness check --config .chrono-harness/ci/initial.json --candidate ROOT_OID --initial`.
For subsequent revisions, run `.chrono-harness/bin/chrono-harness check --config .chrono-harness/ci/check.json --base BASE_OID --candidate CANDIDATE_OID`.
The generated workflow invokes the same commands. Regenerate it with `.chrono-harness/bin/chrono-ci generate --host-root . --config .chrono-harness/ci/github.json`.

This example explicitly supports macOS arm64 and `macos-14`. The initial judge digest is pinned for that platform. Initial inventory completion does not activate full governance, prove input closure, or establish deterministic local/CI parity. The full registries remain proposed. A normal documentation DELTA requires no business tests.

Core agent methods are generated into `CLAUDE.md`; `AGENTS.md` is its relative symbolic link. Edit the registered instruction catalog or manifest and run `.chrono-harness/bin/chrono-instructions generate --host-root .`.

The first published root is `4ee7954241eb3c4a40e6cff2c8d2d67beb390a9a`. Later documentation changes use the ordinary DELTA profile with explicit base and candidate commits; the initial inventory is reserved for the parentless root.

## Registered worktrees

The pinned release also installs `chrono-worktree`. The host policy is
`.chrono-harness/worktree.json`; shared registries explicitly declare `dev`,
`feature/`, `integration/`, file ownership and artifacts. Project and FILEMAP
registrations have one owner; directory names and languages do not select work.

```sh
.chrono-harness/bin/chrono-worktree start --host-root . --config .chrono-harness/worktree.json --kind feature --name change --path ../my-change
```

The destination must not exist. `reconstruct` uses the same arguments plus
`--plan .chrono-harness/state/reconstruction.json`, with explicit fixed base and
candidate OIDs and a complete carry/retire path list. See the
[worktree contract](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/worktree.md).
Creation/reconstruction records actual Git results and preserves old work;
reconstruction stages changes and requires a new commit and the canonical check.
PR creation and merge remain caller-owned. Shared full-governance
registries are proposed; worktree use does not activate them or establish full
input closure, freshness certification or deterministic local/CI parity.

The historical parentless root keeps its own beta.5 lock and initial profile; reproduce it from that checkout. This beta.19 adoption uses ordinary DELTA checks and does not claim a new first-root inventory.

## Registered maintenance

The same installed `chrono-worktree` consumes explicit maintenance plans under
`.chrono-harness/state/` with the registered `.chrono-harness/worktree.json`:

```sh
.chrono-harness/bin/chrono-worktree recover --host-root . --config .chrono-harness/worktree.json --plan .chrono-harness/state/recover.json
.chrono-harness/bin/chrono-worktree cleanup --host-root . --config .chrono-harness/worktree.json --plan .chrono-harness/state/cleanup.json
.chrono-harness/bin/chrono-worktree cleanup-fetch --host-root . --config .chrono-harness/worktree.json --plan .chrono-harness/state/cleanup-fetch.json
```

Recovery validates the original failure, reconciled HEAD/index and owned lock;
staged changes still need a candidate commit and the canonical check. Cleanup
requires an explicit retained branch/commit and selected disposable artifacts.
Fetch-ref cleanup requires its original failed receipt and a fixed local branch
preserving the expected commit. Reports retain failures and distinguish verified
removal from unverified partial effects. See the pinned
[maintenance contract](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/worktree.md#registered-recovery-and-cleanup)
for complete plan formats. Lost recovery identity, damaged Git metadata and
PR/merge orchestration remain separate obligations.


## Interrupted operations

The installed tool writes separate immutable intents before checkout/lock effects
and before fetching. After establishing that the original process stopped, supply
an explicit intent digest and original-result presence/digest to:

```sh
.chrono-harness/bin/chrono-worktree recover-interrupted --host-root . --config .chrono-harness/worktree.json --plan .chrono-harness/state/interrupted-checkout.json
.chrono-harness/bin/chrono-worktree cleanup-fetch-interrupted --host-root . --config .chrono-harness/worktree.json --plan .chrono-harness/state/interrupted-fetch.json
```

Checkout recovery also requires the reconciled HEAD/index tree. Fetch cleanup
requires the expected current OID and a local branch retaining it; an already
absent ref needs an explicit retry plan. Both preserve the original bytes and
keep the original outcome unknown; terminal reports use ordinary maintenance.
See the pinned [interruption contracts](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/worktree.md#interrupted-checkout-recovery).
These commands do not reconstruct a lost index, make concurrent writers atomic,
or certify full governance or deterministic parity.

The pinned release also provides optional explicitly bound Git readers. This host keeps its registered scoped profile; adopting new binaries does not implicitly change the Git-binding or governance policy. See the pinned [Git facts contract](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/git-facts.md).

## CI projections and remote retirement

The pinned beta.19 binaries also provide explicit release-workflow generation and full-context CI transport. This host retains its registered scoped profile; installing binaries does not activate full governance. See the pinned [release CI](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/release-ci.md) and [full context CI](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/full-ci.md) contracts.

`chrono-worktree cleanup-remote` consumes an explicit state plan with the expected remote URL, work-branch OID and retained target commit. It performs exact leased deletion, verifies absence and preserves original failures; this is not an atomic remote transaction or a PR/merge verdict. See [remote retirement](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/worktree.md#remote-branch-retirement).

## Literal checkout and metadata recovery

The pinned binaries compare registered Git-tree/index identities with physical bytes, file types and owner executable bits. Git configuration cannot silently normalize changed inputs for this comparison; checkouts must materialize the registered exact bytes.

`chrono-worktree inspect-rebind` and `rebind` use an explicit branch, HEAD, chosen index tree, backup and donor to repair missing or damaged linked-checkout metadata while preserving observed work. The released `chrono-worktree resume-rebind` command continues an interrupted or failed rebind only from its retained intent and original plan; it does not infer a new index, backup, donor or ownership choice. These commands do not infer the lost historical index or original outcome. See [metadata rebind](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/worktree.md#explicit-metadata-rebind) and [literal identity](https://github.com/ChronoAIProject/chrono-harness/blob/v0.1.0-beta.19/docs/git-facts.md#literal-checkout-identity).

This example retains its explicit initial-inventory contract and has no execution plans or scripts. The public binary upgrade does not create empty CI units or adopt a scoped profile in place of the initial contract.
