<script setup lang="ts">
import { computed } from "vue";
type BaseButtonProps = {
  size?: number;
  color?: string;
};

const props = withDefaults(defineProps<BaseButtonProps>(), {
  size: 16,
  color: "skyblue",
});

const fontSize = computed(() => `${props.size}px`);
</script>

<template>
  <button class="button-primary">
    <slot />
  </button>
</template>

<style>
</style>
