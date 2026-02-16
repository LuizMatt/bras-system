<script setup lang="ts">
defineProps<{
  label: string
  href: string
}>()
</script>

<template>
  <NuxtLink 
    :to="href" 
    class="text-muted-foreground hover:text-foreground transition-colors text-sm font-medium"
  >
    {{ label }}
  </NuxtLink>
</template>
