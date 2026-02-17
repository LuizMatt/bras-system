<script setup lang="ts">
import WhatsAppIcon from '../atoms/WhatsAppIcon.vue'
import ButtonLabel from '../atoms/ButtonLabel.vue'

defineProps<{
  variant?: 'full' | 'icon-only'
}>()
</script>

<template>
  <button 
    v-if="variant === 'icon-only'"
    class="bg-gold hover:bg-gold/90 text-gold-foreground p-2.5 rounded-lg transition-colors"
  >
    <WhatsAppIcon :size="20" />
  </button>
  <button 
    v-else
    class="bg-gold hover:bg-gold/90 text-gold-foreground px-6 py-2.5 rounded-lg flex items-center justify-center gap-2 transition-colors"
  >
    <WhatsAppIcon :size="20" />
    <ButtonLabel text="Falar no WhatsApp" />
  </button>
</template>
