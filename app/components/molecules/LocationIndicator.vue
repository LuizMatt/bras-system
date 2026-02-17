<script setup lang="ts">
import AppIcon from '../atoms/AppIcon.vue'
import AppText from '../atoms/AppText.vue'
import StatusDot from '../atoms/StatusDot.vue'

defineProps<{
  label: string
  location: string
}>()
</script>

<template>
  <div class="bg-white rounded-xl px-4 py-3 flex items-center gap-3 shadow-sm">
    <div class="flex items-center justify-center w-10 h-10 bg-green-500/10 rounded-lg">
      <AppIcon name="map-marker" :size="20" class="text-green-500" />
    </div>
    <div class="flex-1">
      <AppText variant="caption" class="text-muted-foreground uppercase tracking-wide">
        {{ label }}
      </AppText>
      <AppText variant="body" class="font-semibold text-foreground">
        {{ location }}
      </AppText>
    </div>
    <StatusDot status="online" />
  </div>
</template>
