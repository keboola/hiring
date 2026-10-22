# Keboola hiring

We hire in the open. Every open role lives as a **branch** in this repository. Apply by opening a **pull request** against that role’s branch, or [reach out privately](#applying-privately) if you prefer to keep your application private.

## How it works

1. Browse open role branches (branch name ≈ role slug, e.g. `ai-transformation-consultant`).
2. Read `JOB_DESCRIPTION.md` on that branch.
3. Fork this repo (or push from a branch you can write to).
4. Open a pull request **into the role branch** (not into `main`).
5. We review the PR as your application. We may ask follow-ups in PR comments.

`main` holds only this process and shared templates. Role-specific content lives on role branches.

## Applying privately

You do not have to submit a public PR if you prefer to keep your job search private. We expect you to take the initiative and figure out how to submit your application privately. Include the role title and the same information requested in `APPLICATION.md` below.

This repository and its pull requests are public. Do not post information you want to keep private.

## What to put in your application PR

Create a folder:

```text
applications/<your-github-username>/
  APPLICATION.md
  CV.pdf          # or CV.md — optional if LinkedIn covers it
```

### `APPLICATION.md` (required)

Use this structure:

```markdown
# Application — <Role title>

- Name:
- Email:
- Location / time zone:
- LinkedIn (or other profile):
- Work authorization / visa notes (optional):

## Why this role

(Short — why Keboola, why this role, why now.)

## One transformation / project you owned

- Problem:
- What you changed:
- Measured result:

## How you work with AI tooling

(Concrete tools and how you use them day to day — not buzzwords.)

## Availability

- Notice period / start date:
- Travel OK for EU client work? (yes/no + notes)
```

Keep it concise. We care what you can do, not where you learned it.

## PR title format

```text
Application: <Role title> — <Your name>
```

Example: `Application: AI Transformation Consultant — Ada Lovelace`

## What happens next

- We acknowledge via PR comment when we’ve seen your application.
- Shortlisted candidates get an interview invite (email or PR comment).
- We close the PR when the process for you ends (hire, decline, or withdrawn). Please don’t reopen closed application PRs; open a new one if a role is still hiring.

## Roles — open and closed

| Role | Branch | Status |
|------|--------|--------|
| AI Transformation Consultant | `ai-transformation-consultant` | Open |

*(Maintainers: add a row when you cut a new role branch.)*

## For Keboola maintainers

### Add a new role

1. Branch from `main`: `git checkout -b <role-slug>`.
2. Add `JOB_DESCRIPTION.md` (and optional `RUBRIC.md` for interviewers — keep private notes out of this public repo).
3. Update the roles table on `main` (via PR to `main`).
4. Before accepting applications, add `refs/heads/<role-slug>` to the active [Preserve role history ruleset](https://github.com/keboola/hiring/rules/25629741). Confirm deletion and force-push protection applies to the new branch; new role branches are not included automatically.
5. Candidates open PRs **into `<role-slug>`**, not into `main`.

### Closing and reopening a role

Role branches are permanent records, not feature branches to merge when hiring ends.

The **Preserve role history** ruleset blocks deletion and force-pushes on registered role branches, with no bypass actors. Normal updates remain allowed. Administrators can still change the ruleset; this is not an immutable backup.

1. Add a dated **Closed** notice to `JOB_DESCRIPTION.md` on the role branch, keeping the job description below it.
2. Keep the role’s row in the roles table on `main` and mark it **Closed** via a PR. Do not remove the row or its branch reference.
3. Close outstanding application PRs with a candidate-facing explanation. Do not merge applications into the role branch or `main`.
4. Keep the role branch and existing PR links. Do not delete the branch, merge it into `main`, force-push, or rewrite its history. Record later changes as new commits.

Job description revisions remain in the role branch’s Git history. Application submissions, reviews, and discussion remain in their PRs; unmerged applications are not part of the role branch itself. A branch alone is not a backup of GitHub PR records.

To reopen the same role, reuse its branch, add a dated **Reopened** notice, and mark its table row **Open** via a PR to `main`. Candidates submit new application PRs rather than reopening closed ones.

Keep private applications and internal assessments outside this public repository. Personal-data removal obligations take precedence over retention; handle any necessary removal separately rather than treating role closure as permission to erase history.

### Reviewing applications

- Treat each PR as confidential candidate data even though the repo is public — don’t paste internal calibration into the PR.
- Prefer structured score notes in your internal ATS / docs; use PR comments for candidate-facing questions only.

## Equal opportunity

Keboola is an equal opportunity employer. If you need accommodations in the hiring process, let us know when you apply.

## Questions

General process questions: open a Discussion. Don’t use application PRs for general Q&A.

---

© Keboola · [keboola.com](https://www.keboola.com) · careers: [keboola.com/about/jobs](https://www.keboola.com/about/jobs)
