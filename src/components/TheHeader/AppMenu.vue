<template>
    <div :class="$style.wrapper">
        <nav :class="$style.menu" v-for="(link, index) in links" :key="index">
            <RouterLink :class="$style.link" :to="link.url">{{ link.text }}</RouterLink>
        </nav>
    </div>
</template>

<script setup>
const links = [
  { text: 'Home', url: '/' },
  { text: 'Blog', url: '/blog' },
  { text: 'Pricing', url: '/pricing'},
  { text: 'Contact', url: '/contact'},
];
</script>

<style module>
.wrapper {
    display: flex;
    align-items: center;
    gap: 54px;
}
.menu {
    display: flex;
    font-family: var(--font-family-secondary);
    font-weight: 500;
    font-size: 17px;
    line-height: 26px;
    color: var(--color-dark);
}
</style>
