# Contributing to Nexus Labs projects

Thank you for helping improve a Nexus Labs project. Contributions are evaluated
on correctness, evidence, maintainability, and their fit with the affected
repository's architecture.

## Before making a change

1. Read the repository README and any local contribution or agent instructions.
2. Search existing issues and pull requests for related work.
3. For a non-trivial change, open or reference an issue that defines the problem
   and expected outcome.
4. Keep the proposed scope narrow enough to validate and reverse safely.

Repository-specific instructions override this document when they are stricter.

## Branches and commits

Use short-lived branches with a descriptive prefix:

- `feat/` for new behavior.
- `fix/` for corrections.
- `docs/` for documentation-only work.
- `refactor/` for behavior-preserving structural changes.
- `test/` for test-only work.
- `chore/` for maintenance.

Prefer focused commits with imperative messages. Conventional Commit prefixes
are encouraged, for example `feat:`, `fix:`, `docs:`, `test:`, and `chore:`.

Do not mix unrelated formatting, generated output, or cleanup into a functional
change unless the pull request explicitly accounts for it.

## Evidence requirements

Every pull request must explain:

- What changed and why.
- What assumptions were made.
- Which commands or checks were run.
- The observed results, including failures or limitations.
- The operational risk and rollback path.
- Whether documentation or runtime migration is required.

Screenshots, logs, traces, and benchmarks should be attached only when they
materially support the claim being made. Redact secrets and personal data.

## Source and runtime separation

Never commit runtime state or machine-local data, including:

- SQLite databases and their `-wal` or `-shm` files.
- Logs, caches, lock files created by running services, or temporary output.
- Backups, memory snapshots, exported user data, or generated evidence bundles.
- Credentials, tokens, private keys, `.env` values, or local tool settings.

Project lockfiles that define reproducible dependencies are source artifacts and
should remain versioned. Runtime lock files are not.

## Pull request workflow

1. Update your branch from the default branch.
2. Run the repository's documented validation and harness commands.
3. Complete the pull request template with concrete evidence.
4. Wait for required automated checks.
5. Resolve review conversations before merge.
6. Prefer squash merge unless preserving individual commits is intentional.

AI-assisted work is welcome, but the author remains responsible for every
change. Repository state, executable checks, and primary documentation are the
sources of truth—not generated summaries or model memory.

## Security

Do not disclose a suspected vulnerability in a public issue. Follow
[`SECURITY.md`](SECURITY.md) and use the affected repository's private security
advisory flow.
