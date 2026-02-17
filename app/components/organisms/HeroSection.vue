<script setup lang="ts">
import HeroContent from './HeroContent.vue'
import VehicleShowcaseCard from './VehicleShowcaseCard.vue'
</script>

<template>
  <section class="bg-navy min-h-screen flex items-center bg-dotted-pattern">
    <div class="max-w-7xl mx-auto px-4 md:px-6 py-12 lg:py-20">
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-16 items-center">
        <!-- Lado Esquerdo: Conteúdo -->
        <HeroContent />

        <!-- Lado Direito: Showcase do Veículo -->
        <VehicleShowcaseCard />
      </div>
    </div>
  </section>
</template>
