# Architecture

Modern single-page application (SPA) built with Vue 3 (Composition API), Vite 8, and TypeScript.

## Component Hierarchy & Atomic Design

The component architecture follows Atomic Design principles:

```text
src/App.vue (Root Layout & Router View)
└── src/views/HomeView.vue (Page View)
    └── src/components/organisms/TheExample.vue (Organism)
        ├── src/components/molecules/TechStackCard.vue (Molecule)
        └── src/components/atoms/SpotlightCard.vue (Atom)
```

- **Atoms (`src/components/atoms/`)**: Primitive building blocks that receive props and render UI with minimal external state (e.g. `SpotlightCard.vue`).
- **Molecules (`src/components/molecules/`)**: Combinations of atoms functioning together as a recognizable unit (e.g. `TechStackCard.vue`).
- **Organisms (`src/components/organisms/`)**: Distinct sections of the UI composed of molecules and atoms (e.g. `TheExample.vue`).
- **Views (`src/views/`)**: Route-level components orchestrated by `vue-router`.

## Routing & State

- **Routing (`src/router/index.ts`)**: Configured with `createRouter` and `createWebHistory` from `vue-router`.
- **State Management**: Uses Pinia (`pinia`) for modular, type-safe reactive state stores.
- **Utilities**: Integrates `@vueuse/core` for composables.

## Build Pipeline

- **Bundler**: Vite 8 with `@vitejs/plugin-vue` and `vite-plugin-vue-devtools`.
- **CSS Engine**: Tailwind CSS v4 via `@tailwindcss/vite`.
