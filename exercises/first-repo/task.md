# Exercise — Lesson 03: Your First Repo

Practice goal: make focused commits using `status`, `add`, and `commit`.

---

## Task A: Make a second commit
1. Add a new line to `README.md`:
```bash
echo "This repo is for my Git workshop." >> README.md
```

2. Review changes:
```bash
git diff
```

3. Stage and commit:
```bash
git add README.md
git commit -m "docs: describe repository purpose"
```

## Task B: Practice staging multiple files
1. Create two files:
```bash
echo "My workshop notes" > notes.txt
echo "TODO: add more lessons" > todo.txt
```

2. Stage only one file:
```bash
git add notes.txt
git status
```

3. Commit only staged work:
```bash
git commit -m "docs: add notes file"
```

4. Stage and commit the remaining file:
```bash
git add todo.txt
git commit -m "chore: add todo list"
```

---

## Expected Result
- You create two additional commits
- Commits stay focused by topic

## Self-Check
- [ ] I used `git diff` before committing
- [ ] I committed `notes.txt` and `todo.txt` separately
- [ ] My commit messages are clear and specific
