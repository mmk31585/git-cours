# Exercise — Lesson 08: Merging Branches

Practice goal: perform both fast-forward and `--no-ff` merges, then inspect the history graph.

## Part A: Create a feature branch and commit
1. Create and switch to a branch:
```bash
git switch -c feature/merge-demo
```

2. Add and commit a file:
```bash
echo "Merge demo content" > merge-demo.txt
git add merge-demo.txt
git commit -m "feat: add merge demo file"
```

## Part B: Merge into main (likely fast-forward)
1. Switch to main:
```bash
git switch main
```

2. Merge:
```bash
git merge feature/merge-demo
```

3. Inspect history:
```bash
git log --oneline --graph --decorate --all
```

Expected result:
- history is often linear for this merge

## Part C: Force a merge commit with `--no-ff`
1. Create another branch:
```bash
git switch -c feature/no-ff-demo
```

2. Add and commit:
```bash
echo "No-ff demo" > no-ff.txt
git add no-ff.txt
git commit -m "feat: add no-ff demo file"
```

3. Merge with `--no-ff`:
```bash
git switch main
git merge --no-ff feature/no-ff-demo
```

4. Inspect history again:
```bash
git log --oneline --graph --decorate --all
```

Expected result:
- a merge commit appears in graph output

## Self-Check
- [ ] I merged a feature branch into `main`
- [ ] I observed a fast-forward or linear merge
- [ ] I forced a merge commit with `--no-ff`
- [ ] I used `git log --graph` to inspect history
