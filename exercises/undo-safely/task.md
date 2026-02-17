# Exercise — Lesson 06: Undo Basics Safely

Practice goal: undo changes safely at file, staging, and history levels.

## Part A: Undo a file change (working tree)
1. Make a change:
```bash
echo "oops change" >> README.md
git status
```

2. Discard it:
```bash
git restore README.md
git status
```

Expected result:
- `README.md` returns to last committed state

## Part B: Unstage a file (staging -> working tree)
1. Modify and stage:
```bash
echo "temp" >> README.md
git add README.md
git status
```

2. Unstage but keep edits:
```bash
git restore --staged README.md
git status
```

Expected result:
- file is modified
- file is not staged

## Part C: Undo a local commit with reset
1. Commit something:
```bash
git add README.md
git commit -m "docs: temporary change"
```

2. Undo commit but keep edits unstaged:
```bash
git reset HEAD~1
git status
```

Expected result:
- commit is removed from `git log`
- changes remain in working tree

## Part D: Undo safely with revert
1. Make a commit:
```bash
git add README.md
git commit -m "docs: add another change"
```

2. Find hash:
```bash
git log --oneline
```

3. Revert commit:
```bash
git revert <commit-hash>
```

Expected result:
- a new commit is created that undoes the target commit

## Part E: Recovery drill with reflog
1. Show reflog:
```bash
git reflog
```

2. Optional advanced step: identify a prior reference and note it.
Practice this only in a disposable clone/test repository (or create a backup branch first), because `--hard` discards working-tree and index changes.
```bash
git reset --hard <reflog-hash>
```

## Self-Check
- [ ] I used `git restore` to discard file edits
- [ ] I used `git restore --staged` to unstage safely
- [ ] I used `git reset` only for local/not-pushed commits
- [ ] I used `git revert` to create an undo commit
- [ ] I know `git reflog` can help recover lost history
