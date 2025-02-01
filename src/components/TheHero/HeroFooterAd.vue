<template>
    <img :class="$style.heroImage" :src="herofooterad" alt="heroimage">
</template>

<script setup>
import herofooterad from '@/assets/images/herofooterad.png';
</script>

<style module>
.heroImage {
    max-width: 301px;
}
</style>
