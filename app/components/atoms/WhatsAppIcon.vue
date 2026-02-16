<script setup lang="ts">
defineProps<{
  size?: number
}>()
</script>

<template>
  <Icon name="mdi:whatsapp" :size="size?.toString() || '20'" />
</template>
