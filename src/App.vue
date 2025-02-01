<template>
  <RouterLink :class="$style.link" to="/">Home</RouterLink>
  <RouterLink :class="$style.link" to="/about">About</RouterLink>
  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style module>
.link {
  font-weight: 700;
  font-size: 28px;
  margin-right: 100px;
  color: red;
}
</style>
