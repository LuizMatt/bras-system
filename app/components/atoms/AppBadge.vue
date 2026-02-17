<script setup lang="ts">
type Variant = 'default' | 'success' | 'warning' | 'info'

withDefaults(defineProps<{
  variant?: Variant
}>(), {
  variant: 'default'
})

const classes: Record<Variant, string> = {
  default: 'bg-muted text-muted-foreground',
  success: 'bg-green-500/10 text-green-500',
  warning: 'bg-gold/10 text-gold',
  info: 'bg-blue-500/10 text-blue-500'
}
</script>

<template>
  <span 
    :class="[
      'inline-flex items-center gap-2 px-3 py-1.5 rounded-full text-sm font-medium',
      classes[variant]
    ]"
  >
    <slot />
  </span>
</template>
