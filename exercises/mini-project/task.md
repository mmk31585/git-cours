# Exercise — Lesson 21: Full Workflow Simulation

Practice goal: simulate a complete team workflow from issue to merged PR.

## Part A: Planning
1. Create GitHub Issue: "Add mini project demo note".
2. Define acceptance criteria in issue body.

## Part B: Implementation branch
1. Start from updated main:
```bash
git switch main
git pull
git switch -c feature/mini-project-demo
```

2. Implement small change:
```bash
echo "Mini project demo" > mini-project.md
git add mini-project.md
git commit -m "feat: add mini project demo note"
```

3. Push:
```bash
git push -u origin feature/mini-project-demo
```

## Part C: PR and review
1. Open PR linked to issue.
2. Add summary and test notes.
3. Apply one follow-up commit (simulate review feedback):
```bash
echo "Updated after review" >> mini-project.md
git add mini-project.md
git commit -m "fix: apply review feedback to mini project"
git push
```

4. Merge PR.

## Part D: Post-merge sync
```bash
git switch main
git pull
```

## Self-Check
- [ ] I linked PR to issue
- [ ] I pushed at least two commits to feature branch
- [ ] PR was reviewed before merge
- [ ] Local `main` is synced after merge
