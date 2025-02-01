<template>
  <header>
    <TheHeader />

    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from '@/components/TheHeader/TheHeader.vue';
</script>

<style module></style>