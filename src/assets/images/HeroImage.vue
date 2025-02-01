<template>
    <img :class="$style.heroImage" :src="imagehero" alt="heroimage">
</template>

<script setup>
import imagehero from '@/assets/images/heroimage.png';
</script>

<style module>
.heroImage {
    max-width: 650px;
}
</style>
