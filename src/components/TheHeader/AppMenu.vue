<template>
    <div :class="$style.wrapper">
        <nav>
            <ul :class="$style.menu">
                <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<script setup>
const links = [
  { text: "Home", url: "/" },
  { text: "About", url: "/about" },
  { text: "Services", url: "/services" },
  { text: "Contact", url: "/contact" },
];
</script>

<style module>
.wrapper {
    display: flex;
    align-items: center;
}
.menu {
    display: flex;
    font-family: var(--font-family-secondary);
    font-weight: 500;
    font-size: 17px;
    line-height: 26px;
    color: var(--color-dark);
    gap: 54px;
}
</style>
