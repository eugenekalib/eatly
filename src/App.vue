<template>
<RouterLink to="/">Home</RouterLink>
<RouterLink to="/about">About</RouterLink>
    <!-- <TheHeader />
\
  <TheHero />

   <AppFeatures /> -->

   <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from '@/components/TheHeader/TheHeader.vue';
import TheHero from './components/TheHero/TheHero.vue';
import AppFeatures from './components/AppFeatures/AppFeatures.vue';
</script>
