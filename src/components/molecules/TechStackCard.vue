<script setup>
import AtomsSpotlightCard from '../atoms/SpotlightCard.vue';

defineProps({
  title: {
    type: String,
    required: true,
  },
  version: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <AtomsSpotlightCard>
    <h2 class="text-lg font-medium mb-2 text-neutral-200">
      {{ title }}
    </h2>
    <p class="text-neutral-500 text-sm mb-4">
      v{{ version }}
    </p>
    <p class="text-neutral-400 leading-relaxed">
      {{ description }}
    </p>
  </AtomsSpotlightCard>
</template>
