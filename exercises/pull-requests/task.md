# Exercise — Lesson 12: Pull Requests

Practice goal: open a pull request and walk through review to merge.

## Part A: Create branch and push
1. Create branch:
```bash
git switch -c feature/pr-demo
```

2. Make a small docs change and commit:
```bash
echo "PR demo change" >> README.md
git add README.md
git commit -m "docs: add pr demo change"
```

3. Push:
```bash
git push -u origin feature/pr-demo
```

## Part B: Open PR (GitHub UI)
1. Open PR from `feature/pr-demo` into `main`.
2. Fill PR title and description:
- what changed
- why
- how tested

3. Request at least one reviewer (or self-review if solo).

## Part C: Merge and clean up
1. Merge PR after checks/review.
2. Delete branch on GitHub.
3. Sync local:
```bash
git switch main
git pull
```

## Self-Check
- [ ] I opened a PR from feature branch to main
- [ ] PR description included context and testing notes
- [ ] I merged and synced local main
- [ ] I understand why PR review matters
