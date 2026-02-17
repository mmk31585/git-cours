# Exercise — Lesson 11: Remote, Push, Pull

Practice goal: connect local repo to GitHub and sync changes correctly.

## Part A: Add and verify remote
1. Check current remotes:
```bash
git remote -v
```

2. Add `origin` if missing:
```bash
git remote add origin <repo-url>
```

3. Verify:
```bash
git remote -v
```

## Part B: Push main branch
```bash
git push -u origin main  # or your repo's default branch
```

If your default branch is not `main`, replace it in the push command above.

Verify tracking:
```bash
git branch -vv
```

## Part C: Pull remote changes
1. Make a small change on GitHub UI (for example edit README).
2. Pull locally:
```bash
git pull
```

3. Verify status:
```bash
git status
```

## Self-Check
- [ ] `origin` is configured correctly
- [ ] I pushed `main` with `-u`
- [ ] I pulled remote updates successfully
- [ ] I can explain push vs pull
