<script setup lang="ts">
type Variant = 'h1' | 'h2' | 'h3' | 'body' | 'caption' | 'logo'
type Tag = 'h1' | 'h2' | 'h3' | 'p' | 'span'

const props = withDefaults(defineProps<{
  variant?: Variant
  tag?: Tag
}>(), {
  variant: 'body',
  tag: 'span'
})

const classes: Record<Variant, string> = {
  h1: 'text-5xl md:text-6xl lg:text-7xl font-bold leading-tight',
  h2: 'text-3xl md:text-4xl lg:text-5xl font-bold',
  h3: 'text-xl md:text-2xl font-semibold',
  body: 'text-base',
  caption: 'text-sm',
  logo: 'text-xl font-bold'
}
</script>

<template>
  <component :is="tag" :class="classes[variant]">
    <slot />
  </component>
</template>
