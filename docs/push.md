# Repository & Push Workflow

Every code change must adhere to consistent commit standards and branch hygiene before pushing.

## 1. Branch Naming

Create short, descriptive branches prefixed with the change type:

```text
feat/short-description
fix/short-description
docs/short-description
chore/short-description
refactor/short-description
```

## 2. Commit Standards

Use focused commits with imperative Conventional Commit messages:

```text
feat: add dark mode toggle component
fix: resolve spotlight card offset on mobile
docs: update architecture with pinia store pattern
chore: update devDependencies
```

## 3. Pre-Push Validation Checklist

- [ ] `bun run type-check` completes with 0 errors.
- [ ] `bun run lint` passes cleanly.
- [ ] `bun run build` completes successfully.
- [ ] Commit message follows Conventional Commits format.
