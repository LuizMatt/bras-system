<script setup lang="ts">
import HeroBadge from '../molecules/HeroBadge.vue'
import AppText from '../atoms/AppText.vue'
import AppButton from '../atoms/AppButton.vue'
</script>

<template>
  <div class="flex flex-col gap-6 lg:gap-8">
    <!-- Badge -->
    <HeroBadge text="Monitoramento inteligente 24h" />

    <!-- Título -->
    <AppText variant="h1" tag="h1" class="text-white">
      Proteção total para o seu veículo, 
      <span class="text-gold">paz de espírito</span> 
      para você
    </AppText>

    <!-- Descrição -->
    <AppText variant="body" class="text-white/80 max-w-xl">
      Rastreamento em tempo real e monitoramento especializado para garantir que seu patrimônio esteja sempre seguro.
    </AppText>

    <!-- CTA Button -->
    <div>
      <AppButton>
        Falar com um especialista
      </AppButton>
    </div>
  </div>
</template>
