<template>
  <header>
    <TheHeader />
        <!-- <RouterLink to="/">Home</RouterLink> -->
  </header>
  <TheHero />
  <!-- <RouterView /> -->
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from '@/components/TheHeader/TheHeader.vue';
import TheHero from './components/TheHero/TheHero.vue';
</script>

<style module></style>