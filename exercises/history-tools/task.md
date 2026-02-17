# Exercise — Lesson 05: `log`, `diff`, `show`

Practice goal: inspect history and changes with confidence before and after commits.

## Part A: Use `diff` like a pro
1. Create a file and commit it:
```bash
echo "line 1" > history.txt
git add history.txt
git commit -m "docs: add history file"
```

2. Make an unstaged change:
```bash
echo "line 2" >> history.txt
```

3. View unstaged changes:
```bash
git diff
```

4. Stage and inspect staged changes:
```bash
git add history.txt
git diff --staged
```

5. Commit:
```bash
git commit -m "docs: add second line to history file"
```

## Part B: Use `log` to read timeline
```bash
git log --oneline
git log --oneline --graph --decorate --all
```

Expected result:
- You see commit hashes and messages in order
- Graph view shows branch structure

## Part C: Use `show` to inspect one commit
1. Copy a hash from `git log --oneline`
2. Run:
```bash
git show <commit-hash>
```

Expected result:
- You see commit metadata and exact line changes

## Self-Check
- [ ] I used `git diff` for unstaged changes
- [ ] I used `git diff --staged` for staged changes
- [ ] I used `git log --oneline` to inspect timeline
- [ ] I used `git show <hash>` to inspect a commit
