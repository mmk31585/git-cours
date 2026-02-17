# Exercise — Lesson 13: Team Workflow

Practice goal: follow a complete feature-branch workflow from branch creation to merge sync.

## Part A: Start clean
```bash
git switch main
git pull
```

## Part B: Feature branch work
1. Create branch:
```bash
git switch -c feature/team-workflow-demo
```

2. Make a small docs change and commit:
```bash
echo "Team workflow notes" > team-workflow.md
git add team-workflow.md
git commit -m "docs: add team workflow notes"
```

3. Push branch:
```bash
git push -u origin feature/team-workflow-demo
```

## Part C: PR and merge
1. Open PR on GitHub.
2. Add summary and testing notes.
3. Merge after review/checks.

## Part D: Post-merge cleanup
```bash
git switch main
git pull
```

## Self-Check
- [ ] I followed branch -> commit -> push -> PR -> merge
- [ ] I used focused commit scope
- [ ] I synced local `main` after merge
