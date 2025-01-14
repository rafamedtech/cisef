<script setup lang="ts">
interface Props {
  title: string;
  description: string;
  image: string;
}

defineProps<Props>();
</script>

<template>
  <UCard
    class="relative overflow-hidden h-96 flex justify-center items-center p-2 group"
    :ui="{ shadow: 'shadow-pinterest' }"
  >
    <section class="z-10 relative">
      <h3 class="text-3xl md:text-5xl font-bold text-gray-100">{{ title }}</h3>
      <p class="text-gray-200 font-light md:text-xl">
        {{ description }}
      </p>
    </section>
    <img
      :src="image"
      alt=""
      class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full group-hover:scale-105 transition-all"
    />
  </UCard>
</template>
