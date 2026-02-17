# Exercise — Lesson 09: Merge Conflicts

Practice goal: create a conflict on purpose, resolve it, and complete the merge safely.

## Part A: Create a conflict scenario
1. Start from `main` and create two branches:
```bash
git switch main
git switch -c feature/conflict-a
```

2. Edit and commit:
```bash
echo "Line from branch A" > conflict-demo.txt
git add conflict-demo.txt
git commit -m "feat: add conflict line from branch A"
```

3. Return to main and create second branch:
```bash
git switch main
git switch -c feature/conflict-b
```

4. Edit the same line differently and commit:
```bash
echo "Line from branch B" > conflict-demo.txt
git add conflict-demo.txt
git commit -m "feat: add conflict line from branch B"
```

## Part B: Trigger and resolve conflict
1. Merge first branch into main:
```bash
git switch main
git merge feature/conflict-a
```

2. Merge second branch (will conflict):
```bash
git merge feature/conflict-b
git status
```

3. Open `conflict-demo.txt`, resolve markers, and keep final content.

4. Mark resolved and finish merge:
```bash
git add conflict-demo.txt
git commit -m "fix: resolve merge conflict in conflict-demo.txt"
```

## Part C: Inspect result
```bash
git log --oneline --graph --decorate --all
```

## Self-Check
- [ ] I triggered a conflict intentionally
- [ ] I removed conflict markers correctly
- [ ] I completed the merge with a resolution commit
- [ ] I can explain the conflict workflow
