# Lesson 10 — GitHub Basics: Repos, Issues, README, Licenses

GitHub hosts your Git repositories online and adds collaboration tools.
This lesson focuses on the core GitHub features every project needs.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what GitHub adds on top of Git
- Create a repository on GitHub
- Understand the purpose of README and LICENSE files
- Use Issues to track work
- Use basic GitHub collaboration features

## Simple Explanation
Git stores project history locally.
GitHub adds:
- remote hosting
- team collaboration
- review and planning tools

Core GitHub objects:
- Repository: the project
- README: project overview and usage
- LICENSE: legal usage terms
- Issue: task, bug, or feature request

## Recommended Repository Setup
When creating a new GitHub repo:
- Add a clear repository name
- Add a README
- Add a LICENSE (MIT is common for open-source learning projects)
- Add a `.gitignore` template if needed

## Key Commands (local + GitHub connection)
```bash
git remote -v
git remote add origin <repo-url>
git push -u origin main
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 10 Task](../../exercises/github-basics/task.md)

## Suggested Commit Messages
- `docs: add project readme`
- `chore: add license file`
- `docs: add issue templates`

## Common Beginner Mistakes
- Creating a repo with no README
- Skipping license selection
- Treating Issues like chat instead of actionable tasks
- Pushing to the wrong GitHub repository URL

## Navigation
- Previous: [Lesson 09 — Handling Merge Conflicts](../merge-conflicts/README.md)
- Next: [Lesson 11 — Connecting Local to GitHub](../remote-push-pull/README.md)
