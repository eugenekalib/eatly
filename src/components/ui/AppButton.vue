<template>
    <button :class="['button', $style[`button-${typeClass}`]]">
        <slot></slot>
    </button>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  type: {
    type: String,
    default: 'primary',
    validator: (value) => ['primary', 'outlined', 'transparent'].includes(value)
  }
});

const typeClass = computed(() => props.type);
</script>

<style module>
.button-primary {
  background-color: var(--color-primary);
  color: var(--color-white);
}

.button-outlined {
  background-color: transparent;
  border: 1.5px solid var(--color-primary);
  color: var(--color-primary);
}

.button-transparent {
  background-color: transparent;
  color: var(--color-dark);
  border: 1.5px solid transparent;
}
</style>
