<script setup lang="ts">
type Variant = 'primary' | 'secondary' | 'ghost'

withDefaults(defineProps<{
  variant?: Variant
}>(), {
  variant: 'primary'
})

const classes: Record<Variant, string> = {
  primary: 'bg-gold hover:bg-gold/90 text-gold-foreground',
  secondary: 'bg-secondary hover:bg-secondary/80 text-secondary-foreground',
  ghost: 'hover:bg-accent hover:text-accent-foreground'
}
</script>

<template>
  <button 
    :class="[
      'px-6 py-2.5 rounded-lg font-semibold transition-colors inline-flex items-center justify-center gap-2',
      classes[variant]
    ]"
  >
    <slot />
  </button>
</template>
