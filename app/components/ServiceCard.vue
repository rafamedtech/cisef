<script setup lang="ts">
interface Props {
  title: string;
  description: string;
  image: string;
}

defineProps<Props>();
</script>

<template>
  <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
    <section class="z-10 relative">
      <h3 class="text-3xl font-bold text-gray-50">{{ title }}</h3>
      <p class="text-gray-100 font-light">
        {{ description }}
      </p>
    </section>
    <img :src="image" :alt="title" class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full" />
  </UCard>
</template>
