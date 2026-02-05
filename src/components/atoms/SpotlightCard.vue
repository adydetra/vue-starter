<script setup>
import { reactive, ref } from 'vue';

const divRef = ref(null);
const position = reactive({ x: 0, y: 0 });
const opacity = ref(0);

function handleMouseMove(e) {
  if (!divRef.value)
    return;

  const div = divRef.value;
  const rect = div.getBoundingClientRect();

  position.x = e.clientX - rect.left;
  position.y = e.clientY - rect.top;
}

function handleMouseEnter() {
  opacity.value = 1;
}

function handleMouseLeave() {
  opacity.value = 0;
}
</script>

<template>
  <div
    ref="divRef"
    class="relative p-6 border border-neutral-800 rounded-lg overflow-hidden group transition-colors duration-300 bg-neutral-900/50"
    @mousemove="handleMouseMove"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
  >
    <div
      class="pointer-events-none absolute -inset-px transition opacity duration-300"
      :style="{
        opacity,
        background: `radial-gradient(600px circle at ${position.x}px ${position.y}px, rgba(255,255,255,0.06), transparent 40%)`,
      }"
    />
    <div class="relative z-10">
      <slot />
    </div>
  </div>
</template>
