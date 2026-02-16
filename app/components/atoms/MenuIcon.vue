<script setup lang="ts">
defineProps<{
  isOpen?: boolean
}>()
</script>

<template>
  <div class="w-6 h-6 flex flex-col justify-center gap-1.5">
    <span 
      class="block h-0.5 bg-foreground transition-all"
      :class="isOpen ? 'rotate-45 translate-y-2' : ''"
    />
    <span 
      class="block h-0.5 bg-foreground transition-all"
      :class="isOpen ? 'opacity-0' : ''"
    />
    <span 
      class="block h-0.5 bg-foreground transition-all"
      :class="isOpen ? '-rotate-45 -translate-y-2' : ''"
    />
  </div>
</template>
