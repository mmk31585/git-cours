# Lesson 17 — Tagging + Releases: Versioning Your Work

Tags mark important commits, usually release points like `v1.0.0`.
They help teams reference stable versions quickly.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what a Git tag is
- Create annotated release tags
- Push tags to remote
- Inspect tagged commits
- Understand basic semantic versioning

## Simple Explanation
Tags are labels attached to specific commits.

Common pattern:
- `vMAJOR.MINOR.PATCH`
- Example: `v1.2.0`

Annotated tags are preferred for releases because they store metadata.

## Key Commands
```bash
git tag
git tag -a v1.0.0 -m "First official release"
git show v1.0.0
git push origin v1.0.0
git push origin --tags
```

Delete a local tag:
```bash
git tag -d v1.0.0
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 17 Task](../../excersises/tagging-releases/task.md)

## Suggested Commit Messages
- `chore: prepare release notes`
- `chore: tag v0.1.0`
- `docs: explain tagging workflow`

## Common Beginner Mistakes
- Using lightweight tags for formal releases unintentionally
- Forgetting to push tags to remote
- Tagging unstable commits

## Navigation
- Previous: [Lesson 16 — Stash for Context Switching](../stash/README.md)
- Next: [Lesson 18 — .gitignore + Repo Hygiene](../gitignore-hygiene/README.md)
