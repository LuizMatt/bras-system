<script setup lang="ts">
import AppButton from '../atoms/AppButton.vue'
import WhatsAppIcon from '../atoms/WhatsAppIcon.vue'

withDefaults(defineProps<{
  variant?: 'full' | 'icon-only'
}>(), {
  variant: 'full'
})
</script>

<template>
  <AppButton v-if="variant === 'icon-only'" class="!p-2.5">
    <WhatsAppIcon :size="20" />
  </AppButton>
  <AppButton v-else>
    <WhatsAppIcon :size="20" />
    <span class="text-sm font-semibold">Falar no WhatsApp</span>
  </AppButton>
</template>
