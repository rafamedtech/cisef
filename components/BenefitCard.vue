<script setup lang="ts">
interface Props {
  title: string;
  icon: string;
}
const { title, icon } = defineProps<Props>();
</script>

<template>
  <UCard
    :ui="{
      background: 'bg-gradient-to-br from-blue-100 to-green-100',
      shadow: 'shadow-pinterest',
      ring: 'dark:ring-gray-200',
    }"
    class="relative overflow-hidden h-96 grid place-content-center p-2"
  >
    <section class="flex flex-col gap-8 py-12">
      <Icon :name="icon" size="64" class="text-green-500" />
      <span class="text-2xl dark:text-black">{{ title }}</span>
    </section>
  </UCard>
</template>
