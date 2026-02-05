<script setup>
import pkg from '../../../package.json';
import MoleculesTechStackCard from '../molecules/TechStackCard.vue';

const techStack = [
  {
    title: 'Vue',
    version: pkg.dependencies.vue.replace('^', ''),
    description: 'The Progressive JavaScript Framework.',
  },
  {
    title: 'Vite',
    version: pkg.devDependencies.vite.replace('^', ''),
    description: 'Next Generation Frontend Tooling.',
  },
  {
    title: 'Tailwind CSS',
    version: pkg.dependencies.tailwindcss.replace('^', ''),
    description: 'A utility-first CSS framework for rapidly building modern websites.',
  },
  {
    title: 'ESLint',
    version: pkg.devDependencies.eslint.replace('^', ''),
    description: 'Find and fix problems in your JavaScript code.',
  },
];
</script>

<template>
  <div class="min-h-screen bg-neutral-950 text-neutral-100 font-sans selection:bg-neutral-800">
    <div class="max-w-3xl mx-auto px-6 py-12">
      <header class="mb-16">
        <div class="w-12 h-12 bg-neutral-100 rounded-full mb-6" />
        <h1 class="text-4xl font-light tracking-tight mb-4 text-neutral-100">
          Vue Starter
        </h1>
        <p class="text-xl text-neutral-400 font-light leading-relaxed">
          A simple, clean starter template focusing on typography and whitespace.
        </p>
      </header>

      <main class="grid gap-8 md:grid-cols-2">
        <MoleculesTechStackCard v-for="tech in techStack" :key="tech.title" v-bind="tech" />
      </main>

      <footer class="mt-20 pt-8 border-t border-neutral-800 text-sm text-neutral-500 flex justify-between items-center">
        <p>&copy; 2026 - {{ new Date().getFullYear() }} Vue Starter. All rights reserved.</p>
        <p>
          by
          <a href="https://www.adydetra.my.id" target="_blank" class="hover:text-neutral-300 transition-colors">adydetra</a>
        </p>
      </footer>
    </div>
  </div>
</template>
