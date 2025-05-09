<script setup lang="ts">
interface Props {
  title: string;
  description: string;
}

defineProps<Props>();
</script>

<template>
  <UCard
    class="overflow-hidden h-96 flex justify-center items-center group"
    :ui="{
      background: 'bg-gradient-to-br from-blue-100 to-green-100',
      body: { padding: 'p-8' },
      shadow: 'shadow-pinterest',
      ring: 'dark:ring-gray-200',
    }"
  >
    <section class="">
      <h3 class="text-3xl font-bold text-dark-strong">{{ title }}</h3>
      <p class="text-dark-medium font-light md:text-xl">
        {{ description }}
      </p>
    </section>
  </UCard>
</template>
