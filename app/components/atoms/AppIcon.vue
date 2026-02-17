<script setup lang="ts">
withDefaults(defineProps<{
  name: string
  size?: number
}>(), {
  size: 24
})
</script>

<template>
  <span class="mdi" :class="`mdi-${name}`" :style="{ fontSize: `${size}px` }" />
</template>
