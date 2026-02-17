<script setup lang="ts">
type Status = 'online' | 'offline' | 'warning'

withDefaults(defineProps<{
  status?: Status
}>(), {
  status: 'online'
})

const classes: Record<Status, string> = {
  online: 'bg-green-500',
  offline: 'bg-gray-400',
  warning: 'bg-gold'
}
</script>

<template>
  <span 
    :class="[
      'w-2 h-2 rounded-full',
      classes[status]
    ]"
  />
</template>
