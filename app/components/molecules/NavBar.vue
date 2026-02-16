<script setup lang="ts">
import { ref } from 'vue'
import LogoIcon from '../atoms/LogoIcon.vue'
import LogoText from '../atoms/LogoText.vue'
import NavLink from '../atoms/NavLink.vue'
import WhatsAppIcon from '../atoms/WhatsAppIcon.vue'
import ButtonLabel from '../atoms/ButtonLabel.vue'
import MenuIcon from '../atoms/MenuIcon.vue'

const navLinks = [
  { label: 'Benefícios', href: '#beneficios' },
  { label: 'Planos', href: '#planos' },
  { label: 'Como Funciona', href: '#como-funciona' }
]

const isMenuOpen = ref(false)
</script>

<template>
  <nav class="bg-background border-b border-border px-4 md:px-6 py-4">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <!-- Logo -->
      <div class="flex items-center gap-2">
        <LogoIcon :size="32" />
        <LogoText text="BRASSYSTEM" />
      </div>

      <!-- Desktop Nav Links -->
      <div class="hidden md:flex items-center gap-6 lg:gap-8">
        <NavLink 
          v-for="link in navLinks" 
          :key="link.href"
          :label="link.label" 
          :href="link.href" 
        />
      </div>

      <!-- Desktop WhatsApp Button -->
      <button class="hidden lg:flex bg-gold hover:bg-gold/90 text-gold-foreground px-6 py-2.5 rounded-lg items-center gap-2 transition-colors">
        <WhatsAppIcon :size="20" />
        <ButtonLabel text="Falar no WhatsApp" />
      </button>

      <!-- Tablet WhatsApp Icon -->
      <button class="hidden md:flex lg:hidden bg-gold hover:bg-gold/90 text-gold-foreground p-2.5 rounded-lg transition-colors">
        <WhatsAppIcon :size="20" />
      </button>

      <!-- Mobile Menu Button -->
      <button 
        @click="isMenuOpen = !isMenuOpen"
        class="md:hidden p-2"
        aria-label="Menu"
      >
        <MenuIcon :isOpen="isMenuOpen" />
      </button>
    </div>

    <!-- Mobile Menu -->
    <div 
      v-if="isMenuOpen"
      class="md:hidden mt-4 pt-4 border-t border-border flex flex-col gap-4"
    >
      <NavLink 
        v-for="link in navLinks" 
        :key="link.href"
        :label="link.label" 
        :href="link.href"
        @click="isMenuOpen = false"
      />
      <button class="bg-gold hover:bg-gold/90 text-gold-foreground px-6 py-2.5 rounded-lg flex items-center justify-center gap-2 transition-colors">
        <WhatsAppIcon :size="20" />
        <ButtonLabel text="Falar no WhatsApp" />
      </button>
    </div>
  </nav>
</template>
