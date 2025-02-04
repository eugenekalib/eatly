<template>
    <div :class="['container']">
        <div :class="$style.wrapper">
            <HeaderLogo />
            <AppMenu :class="$style.menu" />
            <div :class="$style.userActions">
                <AppButton type="transparent">Login</AppButton>
                <AppButton type="primary">Sign up</AppButton>
            </div>
        </div>
    </div>
</template>
  
<script setup>
import AppMenu from './AppMenu.vue';
import HeaderLogo from './HeaderLogo.vue';
import AppButton from '@/components/ui/AppButton.vue';
</script>

<style module>
.wrapper {
    display: flex;
    border-bottom: 1px solid var(--color-white-dark);
    padding-top: 48px;
    padding-bottom: 26px;
}
.menu {
    margin-left: 103px;
}
.userActions {
    margin-left: auto;
}


@media screen and (max-width: 768px) {
    .container {
        padding-inline: 20px;
    }
}
</style>
