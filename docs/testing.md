# Development & Quality Assurance

Commands and workflows for type checking, linting, and build validation.

## Commands

```bash
# Run local development server with HMR
bun run dev

# Run TypeScript type check
bun run type-check

# Run ESLint validation
bun run lint

# Auto-fix ESLint issues
bun run lint:fix

# Run production build (type-check + vite build)
bun run build

# Preview production build locally
bun run preview
```

## Quality Checklist

Before opening a pull request or pushing commits:
1. Ensure `bun run type-check` reports 0 TypeScript diagnostics.
2. Ensure `bun run lint` passes without warnings or errors.
3. Verify `bun run build` generates the production bundle into `dist/`.
