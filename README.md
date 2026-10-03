# Vue Starter ⚡

![Static Badge](https://img.shields.io/badge/license-MIT-brightgreen?label=LICENSE)
[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/adydetra/vue-starter)

A lightweight Vue starter template built with Vite and Tailwind CSS. Fast development environment with HMR (Hot Module Replacement) and modern tooling out of the box.

---

## Features

- ⚡ **Vite** - Next generation frontend tooling
- 🟢 **Vue 3** - The Progressive JavaScript Framework (Composition API)
- 🍍 **Pinia** - Intuitive, type-safe state management
- 🔀 **Vue Router** - Official client-side routing
- 🎨 **Tailwind CSS** - Utility-first CSS framework
- 📝 **ESLint** - Code quality and consistency
- 🔥 **HMR** - Fast refresh during development

---

## Project Structure

```text
├── docs/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── atoms/
│   │   ├── molecules/
│   │   └── organisms/
│   ├── router/
│   ├── views/
│   ├── App.vue
│   ├── index.css
│   └── main.ts
├── AGENTS.md
├── index.html
├── package.json
└── vite.config.ts
```

---

## Getting Started

### Requirements

- [Node.js](https://nodejs.org/) (LTS recommended)
- npm, yarn, pnpm, or bun

### Install dependencies

```bash
npm install
```

### Run the development server

```bash
npm run dev
```

The development server will start at `http://localhost:5173`

---

> [!NOTE]
> Prefer using another package manager? Use one of the following:
>
> ```bash
> yarn install
> # or
> pnpm install
> # or
> bun install
> ```

---

## Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build for production
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint to check code quality

---

## License

This project is licensed under the [MIT](LICENSE) license.
