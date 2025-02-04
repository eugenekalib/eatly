<template>
    <div :class="$style.wrapper">
        <div :class="['container', $style.list]">
            <div :class="$style.item" v-for="(text, index) in features" :key="index">
                <h2 :class="$style.heading">{{ text.head }}</h2>
                <p :class="$style.text">{{ text.text }}</p>
            </div>
        </div>
    </div>
</template>

<script setup>
const features = [
  { head: '10K+', text: 'Satisfied Costumers All Great Over The World'},
  { head: '4M', text: 'Healthy Dishes Sold Including Milk Shakes Smooth'},
  { head: '99.99%', text: 'Reliable Customer Support We Provide Great Experiences'},
];
</script>

<style module>
.wrapper {
    background-color: var(--color-blue-purple);
}
.list {
    display: flex;
    gap: 132px;
    padding-top: 49px;
    padding-bottom: 49px;
    justify-content: center;
}
.item {
    max-width: 260px;
    color: var(--color-white);
    text-align: center;
    /* border-right: 1px solid #ddd;  */
}
.heading {
    font-family: sans-serif;
    font-weight: 700;
    font-size: 44px;
    line-height: 54px;
}
.text {
    padding-top: 10px;
    font-family: Inter;
    font-size: 14px;
    font-weight: 500;
    line-height: 21.6px;
    max-width: 203px;
    text-align: center;
}
</style>
