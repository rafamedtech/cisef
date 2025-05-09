<script setup lang="ts">
import { Motion } from 'motion-v';
import type { IntrinsicElementAttributes } from 'vue';

const { variants } = defineProps<{
  variants: {
    hidden: { opacity: number };
    visible: { opacity: number };
  };
  as?: keyof IntrinsicElementAttributes | undefined;
}>();
</script>

<template>
  <Motion
    :variants="variants"
    initial="hidden"
    animate="visible"
    :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
    :as="as"
  >
    <slot />
  </Motion>
</template>
