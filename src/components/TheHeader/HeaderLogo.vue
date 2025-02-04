<template>
    <div :class="$style.wrapper">
        <LogoImage />
        <div :class="$style.text">
            <p>eatly</p>
        </div>
    </div>
</template>

<script setup>
import LogoImage from '@/assets/images/LogoImage.vue';
</script>

<style module>
.wrapper {
    display: flex;
    align-items: center;
}
.text {
    margin-left: 11px;
    font-weight: 600;
    font-size: 21px;
    line-height: 28px;
    color: var(--color-primary);
}
</style>
