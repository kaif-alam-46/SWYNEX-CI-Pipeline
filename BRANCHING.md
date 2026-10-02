# Git Branching Notes

## Branches

### main
Contains stable, submission/release-ready code.

### develop
Used to integrate completed features before they are merged into `main`.

### feature/*
Used for individual features or changes.

Example:

```text
feature/sample-app
feature/update-readme
feature/add-tests
```

## Recommended Workflow

1. Start from `develop`.
2. Create a feature branch.
3. Make the required changes.
4. Commit changes with a clear message.
5. Push the feature branch to GitHub.
6. Create a Pull Request into `develop`.
7. After testing/review, merge into `develop`.
8. When the project is ready, merge `develop` into `main`.

Example commands:

```bash
git checkout develop
git pull origin develop
git checkout -b feature/sample-app

# make changes

git add .
git commit -m "feat: add sample app"
git push -u origin feature/sample-app
```

## Commit Message Style

Use short, descriptive messages such as:

- `feat: add sample application`
- `docs: update README`
- `fix: correct server response`
- `chore: update gitignore`
