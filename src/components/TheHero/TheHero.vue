<template>
    <div :class="['container', $style.wrapper]">
        <div :class="$style.text">
            <p :class="$style.ad">OVER 1000 USERS</p>
            <h2 :class="$style.heading">Enjoy Foods All Over The World</h2>
            <p :class="$style.description">EatLy help you set saving goals, earn cash back offers, Go to disclaimer for more details and get paychecks up to two days early. Get a $20 bonus.</p>
            <AppButton :class="$style.button" type="primary">Get started</AppButton>
            <AppButton type="outlined">Go Pro</AppButton>
            <img :class="$style.footer" src="@/images/herofooterad.png" alt="">
        </div>
        <div :class="$style.images">
            <img src="@/images/dish1little.png" alt="" :class="$style.image">
            <SmallDishCard :dish="{
                image: '@/images/dish1little.png',
                title: 'Chicken Hell',
                status: 'On The Way',
                time: '3:09 pm'
            }"/>
        </div>
    </div>
</template>

<script setup>
import AppButton from '@/components/ui/AppButton.vue';
import SmallDishCard from '@/components/AppCard/SmallDishCard.vue';
</script>

<style module>
.wrapper {
    margin-top: 49px;
    display: flex;
    margin-bottom: 130px;
}
.text {
    margin-top: 70px;
    max-width: 590px;
}
.ad {
    color: var(--color-dark-lighter);
    font-weight: 600;
    font-size: 15px;
    line-height: 18px;
    max-height: 100%;
}
.ad::before {
    content: "";
    display: inline-block;
    width: 54px;
    height: 1px;
    background-color: var(--color-dark-lighter);
    margin-right: 20px;
    vertical-align: middle;
}
.heading {
    padding-top: 18px;
    font-weight: 600;
    font-size: 75px;
    line-height: 90px;
    font-family: var(--font-family-primary);
}
.description {
    font-family: var(--font-family-secondary);
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    color: var(--color-dark);
    padding-top: 16px;
    max-width: 500px;
}
.button {
    margin-right: 18px;
    margin-top: 53px;
}
.footer {
    padding-top: 33px;
    max-width: 301px;
}
.image {
    max-width: 422px;
    max-height: 422px;
    padding-top: 19px;
    margin-left: 175px;
}
</style>
