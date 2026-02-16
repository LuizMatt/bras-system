<script setup lang="ts">
defineProps<{
  text: string
}>()
</script>

<template>
  <span class="text-sm font-semibold">{{ text }}</span>
</template>
