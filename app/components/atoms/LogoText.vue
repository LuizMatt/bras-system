<script setup lang="ts">
defineProps<{
  text: string
}>()
</script>

<template>
  <span class="text-xl font-bold">
    <span class="text-navy">BRAS</span><span class="text-gold">{{ text.slice(4) }}</span>
  </span>
</template>
