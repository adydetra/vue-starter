# Agent Guide

Vue 3 + Vite 8 starter template with TypeScript, Tailwind CSS v4, Pinia, Vue Router, and atomic design components.

Read only the document needed:
- `docs/architecture.md`: atomic design hierarchy (atoms, molecules, organisms), router, state management, and asset pipeline.
- `docs/style.md`: Tailwind CSS v4 setup with `@tailwindcss/vite`, global CSS, and utility conventions.
- `docs/testing.md`: linting commands, TypeScript type checking, and production build verification.
- `docs/push.md`: branch naming, commit standards, pull request lifecycle, and pre-push validation.
- `docs/status.md`: implemented features, key dependencies, and roadmap.

## Source Map

- `src/main.ts`: application entry point, Pinia store registration, router mounting, and style imports.
- `src/App.vue`: root layout and router view container.
- `src/router/index.ts`: Vue Router route definitions and history mode configuration.
- `src/views/HomeView.vue`: home route page rendering component organisms.
- `src/components/atoms/SpotlightCard.vue`: atomic card component with mouse-tracking radial gradient glow.
- `src/components/molecules/TechStackCard.vue`: molecular card showing technology badges and details.
- `src/components/organisms/TheExample.vue`: organism component composing atoms and molecules into showcase layouts.
- `src/index.css`: Tailwind CSS v4 imports and custom base utility styles.
- `vite.config.ts`: Vite configuration with Vue, Vue DevTools, and Tailwind CSS plugins.
- `package.json`: scripts and dependency declarations.

## Invariants

- Use Vue 3 Composition API with `<script setup lang="ts">`.
- Follow atomic design principles: keep atoms presentational, molecules composite, and organisms domain-aware.
- Prefer Tailwind utility classes over ad-hoc CSS. Use scoped styles only when CSS variables or complex dynamic transforms require it.
- Keep state scalable: use Pinia stores for cross-component shared state; do not clutter components with global state.
- Ensure strict TypeScript compliance: all code must pass `bun run type-check` (`vue-tsc --build`) without errors.
- Adhere to `@antfu/eslint-config` formatting and linting rules (`bun run lint`).

## Change Workflow

Read `package.json` before altering dependencies or scripts. Run `bun run type-check` and `bun run lint` before committing any code changes. Follow `docs/push.md` for git conventions, and keep `docs/` updated if architectural invariants change.
