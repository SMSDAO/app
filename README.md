# Release Process

This document defines the **canonical release workflow** for the SMSDAO Social Portfolio Platform.  
It mirrors the governance and CI discipline used in your other ecosystem repos (e.g. CyberAi).

---

## 1. Release Principles

- **Deterministic:** Same inputs → same build → same behavior.
- **Additive‑first:** Prefer additive changes; removals require explicit justification.
- **Documented:** Every meaningful change must be reflected in `docs/`.
- **Guarded:** Protected branches are only updated via PRs with passing checks.
- **Reversible:** Every release must be traceable and roll‑backable.

---

## 2. Branch Model

- **`main`**
  - Always deployable.
  - Protected: requires PR + passing checks.
- **Feature branches**
  - Named by purpose, e.g. `feature/top-eight-editor`, `fix/leaderboard-pagination`.
- **Copilot / automation branches**
  - e.g. `copilot/build-social-wallet-platform`.
  - Subject to the same rules as human branches.

---

## 3. Required Checks

For any PR targeting `main`, the following must pass:

- **Type check** (TypeScript)
- **Lint** (ESLint)
- **Tests** (Vitest / Testing Library)
- **Security scan** (e.g. Snyk / custom workflow)
- **Docs build** (`build-docs`)
- **AI review** (advisory but preferred green)

If any required check fails, the PR is **not** merged unless an admin performs an explicit override.

---

## 4. Standard Release Flow

1. **Create branch**
   - From `main`
   - Name clearly: `feature/*`, `fix/*`, `chore/*`, `copilot/*`.

2. **Implement changes**
   - Keep commits focused and small.
   - Update or add docs under `docs/` as needed.
   - Maintain type safety and invariants from `ARCHITECTURE_FULL_SPECS.md`.

3. **Run checks locally (recommended)**
   - `bun lint`
   - `bun test`
   - `bun typecheck` (or equivalent)
   - `bun run build`

4. **Open Pull Request**
   - Target: `main`
   - Include a clear description:
     - What changed
     - Why it changed
     - Any migrations or risks

5. **CI runs**
   - All required workflows execute:
     - tests, lint, typecheck, security, docs, AI review.

6. **Review**
   - At least one human review for non‑trivial changes.
   - Confirm:
     - No unintended logic removal
     - Contracts and APIs remain consistent
     - Docs are updated

7. **Merge**
   - Use **“Squash and merge”** or **“Merge commit”** per repo convention.
   - Only when all required checks are green (or explicit admin override).

8. **Deploy**
   - `main` is automatically deployed via Vercel (or configured target).
   - Verify health checks and basic smoke tests.

---

## 5. Hotfix Process

Hotfixes are for **urgent production issues** only.

1. Branch from `main`: `hotfix/<issue>`
2. Fix the issue with minimal surface area.
3. Run at least:
   - Type check
   - Lint
4. Open PR to `main` with clear “HOTFIX” label.
5. Merge once critical checks pass.
6. Deploy immediately.
7. Follow up with:
   - Tests
   - Docs
   - Post‑mortem if needed.

---

## 6. Versioning & Tags (Optional)

If/when semantic versioning is adopted:

- Tag releases as `vX.Y.Z`.
- Maintain a `CHANGELOG.md` summarizing:
  - Added
  - Changed
  - Fixed
  - Removed

Tags should be created **only after** a successful deployment from `main`.

---

## 7. Governance & Exceptions

- Any deviation from this process must be:
  - Explicitly documented in the PR description.
  - Approved by a maintainer/admin.
- Large, structural changes (e.g. new architecture, new integrations) must:
  - Update `ARCHITECTURE.md`
  - Update `ARCHITECTURE_FULL_SPECS.md`
  - Optionally add or update specs under `docs/specs/`.

---

## 8. Checklist for Every Release

Before merging into `main`, confirm:

- [ ] All required CI checks are green
- [ ] Docs updated (`docs/` where relevant)
- [ ] No unreviewed breaking changes
- [ ] No stray debug logs or test code
- [ ] Contracts and APIs remain consistent
- [ ] Rollback path is clear (previous `main` commit)

This process is the **source of truth** for how changes move from idea → code → production in this repo.
