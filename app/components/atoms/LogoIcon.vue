<script setup lang="ts">
defineProps<{
  size?: number
}>()
</script>

<template>
  <img 
    src="/logo.webp" 
    alt="BrasSystem Logo" 
    :width="size || 32" 
    :height="size || 32"
    class="object-contain"
  />
</template>
