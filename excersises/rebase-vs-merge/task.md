# Exercise — Lesson 15: Rebase vs Merge

Practice goal: compare merge and rebase outcomes on a local branch.

## Part A: Prepare branch
1. Create demo branch:
```bash
git switch -c feature/integration-demo
echo "integration demo" > integration-demo.txt
git add integration-demo.txt
git commit -m "docs: add integration demo file"
```

2. Update main separately:
```bash
git switch main
echo "main update" > main-update.txt
git add main-update.txt
git commit -m "chore: add main update file"
```

## Part B: Merge path
```bash
git switch feature/integration-demo
git merge main
git log --oneline --graph --decorate --all
```

## Part C: Rebase path (fresh branch suggested)
1. Recreate or reset demo branch state, then:
```bash
git rebase main
git log --oneline --graph --decorate --all
```

2. If rebase interrupts:
```bash
git rebase --continue
git rebase --abort
```

## Self-Check
- [ ] I tested merge integration
- [ ] I tested rebase integration
- [ ] I compared history graphs
- [ ] I understand tradeoffs of each approach
