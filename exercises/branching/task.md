# Exercise — Lesson 07: Branching Fundamentals

Practice goal: create a feature branch, commit on it, and switch between branches safely.

## Part A: Create and switch to a branch
1. Ensure you are on main:
```bash
git switch main
```

2. Create and switch:
```bash
git switch -c feature/dark-mode
```

3. Confirm branch:
```bash
git branch
git status
```

Expected result:
- current branch is `feature/dark-mode`

## Part B: Commit on your feature branch
1. Create a feature note:
```bash
mkdir -p features
echo "# Dark Mode" > features/dark-mode.md
echo "This is a draft for dark mode feature." >> features/dark-mode.md
```

2. Stage and commit:
```bash
git add features/dark-mode.md
git commit -m "feat: add dark mode draft"
```

Expected result:
- commit exists on feature branch only

## Part C: Switch back to main and compare
1. Switch back:
```bash
git switch main
```

2. Check branch state:
```bash
git status
```

3. Switch back to feature branch:
```bash
git switch feature/dark-mode
git status
```

Expected result:
- branch switching works cleanly
- `HEAD` points to whichever branch you switched to

## Self-Check
- [ ] I created a branch with `git switch -c`
- [ ] I committed on the feature branch
- [ ] I switched between `main` and feature branch
- [ ] I can explain what `HEAD` means
