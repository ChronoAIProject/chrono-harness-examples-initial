# chrono-harness initial-host example

A documentation-only host demonstrating the generated first-root inventory profile and subsequent DELTA checks with public chrono-harness v0.1.0-beta.5. There are no production or test projects. All tracked files are explicitly registered; no project structure or language is inferred.

Install the pinned public release with `python3 .chrono-harness/install.py .`.
For the parentless root commit, run `.chrono-harness/bin/chrono-harness check --config .chrono-harness/ci/initial.json --candidate ROOT_OID --initial`.
For subsequent revisions, run `.chrono-harness/bin/chrono-harness check --config .chrono-harness/ci/check.json --base BASE_OID --candidate CANDIDATE_OID`.
The generated workflow invokes the same commands. Regenerate it with `.chrono-harness/bin/chrono-ci generate --host-root . --config .chrono-harness/ci/github.json`.

This example explicitly supports macOS arm64 and `macos-14`. The initial judge digest is pinned for that platform. Initial inventory completion does not activate full governance, prove input closure, or establish deterministic local/CI parity. The full registries remain proposed. A normal documentation DELTA requires no business tests.

Core agent methods are generated into `CLAUDE.md`; `AGENTS.md` is its relative symbolic link. Edit the registered instruction catalog or manifest and run `.chrono-harness/bin/chrono-instructions generate --host-root .`.

The first published root is `4ee7954241eb3c4a40e6cff2c8d2d67beb390a9a`. Later documentation changes use the ordinary DELTA profile with explicit base and candidate commits; the initial inventory is reserved for the parentless root.
