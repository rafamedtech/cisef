<script setup lang="ts">
interface CarouselProps {
  items: string[];
}

const { items } = defineProps<CarouselProps>();

const carouselRef = ref();

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return;

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0);
    }

    carouselRef.value.next();
  }, 2500);
});
</script>

<template>
  <UCarousel
    ref="carouselRef"
    v-slot="{ item }"
    :items="items"
    :ui="{ item: 'basis-full' }"
    class="rounded-lg overflow-hidden max-w-[20rem] mx-auto"
  >
    <img :src="item" class="h-[30rem] object-cover rounded-2xl w-full" draggable="false" />
  </UCarousel>
</template>
