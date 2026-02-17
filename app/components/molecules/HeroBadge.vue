<script setup lang="ts">
import AppBadge from '../atoms/AppBadge.vue'
import StatusDot from '../atoms/StatusDot.vue'

defineProps<{
  text: string
}>()
</script>

<template>
  <div class="inline-flex">
    <AppBadge variant="info" class="bg-white/10 backdrop-blur-sm border border-white/20">
      <StatusDot status="online" />
      <span class="text-sm">{{ text }}</span>
    </AppBadge>
  </div>
</template>
