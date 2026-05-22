# Contribution Guide — dabetai

## Our Flow (GitHub Flow)

Simple and direct:

1. Create your **branch** from `main`.
2. Make **commits** in English with conventional commits.
3. Open a **pull request (PR)**.
4. Get **approval**.
5. **Merge** and done.

---

## Naming: Branches and Commits

### Branches

| Prefix     | Use                | Examples                   |
| :--------- | :----------------- | :------------------------- |
| `feat/`    | New features       | `feat/user-onboarding`     |
| `fix/`     | Bug fixes          | `fix/login-validation`     |
| `refactor/`| Code improvements  | `refactor/database-queries`|
| `docs/`    | Documentation      | `docs/api-endpoints`       |
| `test/`    | Tests              | `test/search-algorithm`    |

### Commits (type: subject)

| Type        | Description                 | Example                               |
| :---------- | :-------------------------- | :------------------------------------ |
| `feat:`     | New features                | `feat: implement user auth`           |
| `fix:`      | Bug fixes                   | `fix: correct cart calc error`        |
| `refactor:` | Code restructuring          | `refactor: modularize order logic`    |
| `docs:`     | Documentation changes       | `docs: update installation guide`     |
| `test:`     | Add or modify tests         | `test: add patient search tests`      |

---

## How to Contribute (Step by Step)

1. **Update `main`:**

   ```bash
   git switch main
   git pull origin main
   ```

2. **Create your branch:**

   ```bash
   git branch feat/new-feature
   git switch feat/new-feature
   ```

3. **Work and commit:**

   ```bash
   git add .
   git commit -m "feat: add patient similarity filter"
   ```

4. **Push your branch to GitHub:**

   ```bash
   git push -u origin feat/new-feature
   ```

5. **Open a pull request (PR):**
   - Go to GitHub.
   - **Use the default template:** Fill in the template when creating the PR.
   - **PR Title:** Clear, follows main commit convention (e.g. `feat: add hybrid search mode`).
   - **Description:**
     - **What:** Summary of changes.
     - **Why:** Justification.
     - **How to test:** Steps for the reviewer.
     - **Notes:** Anything extra (e.g. breaking changes, impact on other services).

---

## To Merge You Need:

- ✅ **Approval** from a team member
- ✅ **No conflicts** with `main`
- ✅ **Correct naming** (branches and commits)
- ✅ **Updated documentation** (if applicable)

---

## Code Review

- **Update:** If changes are requested, respond and update your PR.

---

## Key Rules

### Before Merging

- **No direct merge to `main` (always via PR)!**
- **Don't merge code that doesn't compile!**
- **Don't merge if it breaks existing functionality!**
- **Mandatory:** Use branch and commit naming conventions.

### After Merging

- **Delete your branch** on GitHub.
- Notify the team about important changes.

---

## Questions?

- Open an **Issue**.
- Contact any team member.
