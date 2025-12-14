# Team Development Guide

This guide explains **how we use Git and GitHub as a team**. Everyone must follow these rules to keep the codebase stable, readable, and easy to maintain.

---

## 1. Core Principles

* `main` is always stable and deployable
* All work happens on feature or bugfix branches
* Every change goes through a Pull Request (PR)
* History should tell a clear story

If you are unsure, **ask before pushing or merging**.

---

## 2. Branch Naming Conventions

### Branch Types

We use the following branch prefixes:

* `feature/` → new features
* `bugfix/` → bug fixes
* `refactor/` → internal code improvements
* `chore/` → tooling, configs, non-code changes

### Branch Name Format

```
<branch-type>/<area>-<short-description>
```

### Examples

```
feature/auth-login
feature/user-profile-api
bugfix/payment-timeout
refactor/db-transactions
chore/add-eslint
```

### Rules

* Always branch from `dev`
* One branch = one task
* Avoid vague names like `feature/test` or `fix-stuff`

---

## 3. Commit Message Guidelines

Commits are **permanent history**. Write them carefully.

### Commit Message Format

```
<type>(<scope>): <short description>
```

### Commit Types

* `feat` → new feature
* `fix` → bug fix
* `refactor` → code restructuring (no behavior change)
* `chore` → tooling/config
* `docs` → documentation

### Examples (Good)

```
feat(auth): add login controller
fix(user): handle missing profile image
refactor(db): extract transaction helper
chore(env): add dotenv configuration
docs(readme): update setup steps
```

### Examples (Bad)

```
fix
update
changes done
final commit
```

### Commit Rules

* One logical change per commit
* Do not commit broken code
* Use present tense ("add", not "added")
* Review `git diff` before committing

---

## 4. Pull Request (PR) Guidelines

All changes must be merged via Pull Requests.

### PR Target

* Source branch: `feature/*`, `bugfix/*`, etc.
* Target branch: `dev`

Never open PRs directly to `main`.

---

## 5. Writing a Good Pull Request

### PR Title

Use the same style as commit messages:

```
feat(auth): add login API
fix(ui): prevent navbar overflow on mobile
```

### PR Description Must Include

* **What** was changed
* **Why** it was needed
* Any **breaking changes**
* Screenshots (for frontend UI changes)

### Example PR Description

```
### What
- Added login API with JWT authentication
- Added password validation

### Why
- Required for user authentication flow

### Notes
- Token expiry set to 15 minutes
```

---

## 6. PR Best Practices

* Keep PRs small and focused
* Do not mix unrelated changes
* Address review comments seriously
* Push fixes to the same branch (no new PR)

---

## 7. Review & Merge Rules

* At least one review is required
* The PR author fixes review comments
* Use **Squash and Merge** unless instructed otherwise
* Delete branch after merge

---

## 8. Common Mistakes to Avoid

* Pushing directly to `main`
* Large PRs with mixed concerns
* Vague commit messages
* Long-lived feature branches
* Ignoring merge conflicts

---

## 9. Conflict Resolution Rule

* Conflicts are normal
* The branch owner resolves conflicts
* Never blindly accept changes

---

## 10. Final Reminder

> `main` is sacred
> `dev` is shared
> Your branch is your responsibility
> PRs are discussions, not just merges

Following this guide ensures clean history, smooth collaboration, and fewer bugs.

Happy coding 🚀
