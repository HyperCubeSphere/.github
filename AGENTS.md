# AGENTS.md

Default guidance for AI coding agents (Claude Code, Codex, Cursor, GitHub Copilot, and similar) working in HyperCubeSphere repositories. Individual repos may extend or override this file.

## Working agreement

- Read `README.md`, `CONTRIBUTING.md`, and any per-repo `AGENTS.md` before changing files.
- Prefer minimal, reversible changes. No drive-by refactors outside the task scope.
- Never commit secrets, credentials, or `.env` files.
- Run tests, lint, and type-check before declaring a task complete.

## Conventions

- Conventional Commits for commit messages and PR titles (`feat:`, `fix:`, `docs:`, `refactor:`, `perf:`, `test:`, `build:`, `ci:`, `chore:`, `revert:`). Append `!` for breaking changes.
- Default branch: `main`. Branches use kebab-case with a type prefix (e.g. `feat-add-rate-limiting`, `fix-mobile-scroll`).
- Match surrounding code style. Do not reformat unrelated lines.

## AI-authored code

- Disclose AI-generated code in the PR description (the pull request template has a dedicated section).
- Treat AI output as a draft: verify behavior, edge cases, and security implications before requesting review.
- Do not paste secrets, customer data, or proprietary IP into third-party AI services.
- Cite sources when an AI tool surfaces them; flag uncertain attribution rather than hide it.

## Quality gates

A change is ready to merge when:

- The PR title follows Conventional Commits.
- All required CI checks pass.
- Tests cover the new or changed behavior.
- Documentation is updated where the change is user-visible.
- A human reviewer has approved.

## Out of scope without explicit approval

- Force pushes to shared branches; rewriting public Git history.
- Major version bumps of runtime, framework, or database.
- Editing `.github/workflows/*` or branch protection rules.
- Releases, package publishes, or infrastructure changes.
