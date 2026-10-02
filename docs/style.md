# Style & Design System

The project uses Tailwind CSS v4 powered by `@tailwindcss/vite`.

## Setup & Configuration

- Styles are loaded from `src/index.css` via `@import "tailwindcss";`.
- Modern CSS variables and theme tokens are defined directly in CSS using `@theme` blocks when customizations are needed.

## Styling Conventions

- **Utility-First**: Prioritize standard Tailwind utility classes for layout, typography, borders, and colors.
- **Responsive Design**: Mobile-first design using standard breakpoints (`sm:`, `md:`, `lg:`, `xl:`).
- **Interactive Effects**: Radial gradients and mouse glow effects are handled with inline dynamic CSS variables mapped to reactive cursor positions (as seen in `SpotlightCard.vue`).
