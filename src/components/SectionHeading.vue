<script setup>
defineProps({
  eyebrow: { type: String, default: '' },
  title: { type: String, required: true },
  description: { type: String, default: '' },
  centered: { type: Boolean, default: false }
})
</script>

<template>
  <div class="section-heading" :class="{ centered }" data-reveal>
    <span class="eyebrow"><span class="eyebrow-mark"></span>{{ eyebrow }}</span>
    <h2>{{ title }}</h2>
    <p v-if="description">{{ description }}</p>
  </div>
</template>
