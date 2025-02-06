<template>
    <div :class="$style.wrapper">
        <img :src="dish.image" :alt="dish.title" :class="$style.image"/>
        <div :class="$style.info">
            <h2 :class="$style.heading">{{ dish.title }}</h2>
            <p :class="$style.text">{{ dish.status }}</p>
        </div>
        <span :class="$style.time">{{ dish.time }}</span>
    </div>
</template>

<script setup>
defineProps({
  dish: {
    type: Object,
    required: true,
    validator: (value) => {
      return (
        typeof value.title === 'string' &&
        typeof value.image === 'string' &&
        typeof value.status === 'string' &&
        typeof value.time === 'string'
      );
    }
  }
});
</script>

<style module>
.wrapper {
    max-width: 328px;
    max-height: 90px;
    background-color: var(--color-white);
    display: flex;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    border-radius: 16px;
}
.image {
    max-height: 80px;
    max-width: 80px;
    margin-top: 4px;
    margin-bottom: 4px;
    margin-left: 16px;
}
.info {
    padding-top: 18px;
    padding-bottom: 24px;
    padding-left: 18px;
}
.heading {
    font-weight: 600;
    font-size: 16px;
    line-height: 22px;
}
.text {
    font-weight: 500;
    font-size: 9px;
    line-height: 14px;
}
.time {
    margin-top: auto;
    margin-left: auto;
    padding-right: 16px;
    padding-bottom: 10px;
    font-weight: 500;
    font-size: 10px;
    line-height: 14px;
    color: var(--color-white-dark);
}
</style>
