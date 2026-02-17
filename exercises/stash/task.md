# Exercise — Lesson 16: Stash

Practice goal: stash work in progress, switch branches, and restore safely.

## Part A: Create WIP changes
1. On a feature branch:
```bash
git switch -c feature/stash-demo
echo "work in progress" > stash-demo.txt
git status
```

2. Save stash with message:
```bash
git stash push -m "wip: stash demo changes"
```

3. Confirm clean tree:
```bash
git status
```

## Part B: Inspect stash
```bash
git stash list
git stash show -p stash@{0}
```

## Part C: Restore stash
1. Apply without deleting:
```bash
git stash apply stash@{0}
```

2. Or pop (apply + remove):
```bash
git stash pop
```

## Part D: Stash untracked files
```bash
echo "temp" > untracked-temp.txt
git stash -u
git stash list
```

## Self-Check
- [ ] I created and named a stash
- [ ] I viewed stash list and contents
- [ ] I restored stash with apply or pop
- [ ] I tested `git stash -u`
