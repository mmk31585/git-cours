# Exercise — Lesson 20: Best Practices Audit

Practice goal: apply a pre-push quality checklist to your repository.

## Part A: Pre-push review
Run:
```bash
git status
git diff
git diff --staged
git log --oneline -n 10
```

## Part B: Improve commit quality
1. If staged changes are mixed, split them into focused commits.
2. Use clear commit messages with `feat/fix/docs/chore`.

## Part C: Hygiene checks
1. Confirm secrets are not tracked.
2. Confirm `.gitignore` covers generated files.

## Part D: Create personal checklist note
```bash
mkdir -p notes
cat > notes/lesson-20-checklist.md << 'EOF'
## Pre-Push Checklist
- status clean enough?
- staged diff reviewed?
- commit messages clear?
- right branch?
- no secrets?
EOF
```

## Self-Check
- [ ] I reviewed status and diffs before push
- [ ] I improved at least one commit message
- [ ] I validated ignore and secret hygiene
- [ ] I documented a reusable checklist
