# Exercise — Lesson 04: Working Tree, Staging, Repository

Practice goal: see the three areas in action and control what enters each commit.

---

## Part A: See the 3 areas in action
1. Create a file:
```bash
echo "line 1" > demo.txt
```

2. Check status:
```bash
git status
```

3. Stage it and check status again:
```bash
git add demo.txt
git status
```

4. Commit and check status:
```bash
git commit -m "docs: add demo file"
git status
```

## Part B: Stage only what you want
1. Create two files:
```bash
echo "BUG FIX: update button label" > bugfix.txt
echo "FEATURE: add dark mode draft" > feature.txt
```

2. Stage only the bugfix and verify:
```bash
git add bugfix.txt
git status
```

3. Commit only the bugfix:
```bash
git commit -m "fix: add bugfix note"
```

4. Commit the feature separately:
```bash
git add feature.txt
git commit -m "feat: add feature draft"
```

## Part C: Unstage but keep edits
1. Edit `feature.txt`:
```bash
echo "more work..." >> feature.txt
```

2. Stage it:
```bash
git add feature.txt
```

3. Unstage it (without losing edits):
```bash
git restore --staged feature.txt
git status
```

---

## Expected Result
- You can identify where changes live: working tree, staging area, or repository
- You can create focused commits by staging selectively
- You can unstage changes safely

## Self-Check
- [ ] I staged and committed `demo.txt`
- [ ] I created separate commits for bugfix and feature
- [ ] I used `git restore --staged` and kept my file edits
