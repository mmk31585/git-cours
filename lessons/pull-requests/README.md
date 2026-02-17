# Lesson 12 — Pull Requests 101: From Branch to Review to Merge

A pull request (PR) is how teams review and merge code safely.
This lesson covers the minimal, practical PR workflow.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what a pull request is
- Open a PR from a feature branch
- Write a clear PR description
- Request review and respond to feedback
- Merge PR safely

## Simple Explanation
A PR is a request to merge changes from one branch into another.

Typical PR flow:
1. Create branch
2. Commit changes
3. Push branch
4. Open PR
5. Review and update
6. Merge

## Key Commands
```bash
git switch -c feature/pr-demo
git add .
git commit -m "feat: add pr demo"
git push -u origin feature/pr-demo
```

## What a Good PR Includes
- clear title
- short summary of what changed
- testing notes
- linked issue (if available)

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 12 Task](../../exercises/pull-requests/task.md)

## Suggested Commit Messages
- `feat: add pr demo change`
- `docs: add pr description checklist`
- `fix: address review feedback`

## Common Beginner Mistakes
- Opening huge PRs with unrelated changes
- Missing context in PR description
- Merging without review in team repos
- Ignoring CI/test failures

## Navigation
- Previous: [Lesson 11 — Connecting Local to GitHub](../remote-push-pull/README.md)
- Next: [Lesson 13 — Team Workflow](../team-workflow/README.md)
