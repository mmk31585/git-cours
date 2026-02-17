# Exercise — Lesson 14: Fetch, Pull, Rebase

Practice goal: sync from remote and update your branch with rebase.

## Part A: Fetch updates
```bash
git fetch origin
git status
```

Inspect graph:
```bash
git log --oneline --graph --decorate --all
```

## Part B: Pull normally
```bash
git switch main
git pull
```

## Part C: Rebase a feature branch
1. Create branch and commit a small change:
```bash
git switch -c feature/rebase-demo
echo "rebase demo" > rebase-demo.txt
git add rebase-demo.txt
git commit -m "docs: add rebase demo note"
```

2. Rebase onto updated main:
```bash
git switch main
git pull
git switch feature/rebase-demo
git rebase main
```

If interrupted:
```bash
git rebase --continue
git rebase --abort
```

## Self-Check
- [ ] I used `git fetch` and inspected history
- [ ] I pulled updates on main
- [ ] I rebased a feature branch onto main
- [ ] I know continue vs abort in rebase flow
