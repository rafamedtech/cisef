<script setup lang="ts">
// const items = [
//   'https://res.cloudinary.com/rafamed-dev/image/upload/v1743211570/cisef/a8163245-b880-4765-baca-5854e3755a29_xyuouz.jpg',
//   'https://res.cloudinary.com/rafamed-dev/image/upload/v1743211571/cisef/fd371189-9e0e-438f-86bb-f779a8e00b5c_tootcy.jpg',
//   'https://res.cloudinary.com/rafamed-dev/image/upload/v1743211571/cisef/aa56fa25-20a1-4f8f-8698-3b723966d838_gghzrf.jpg',
//   'https://res.cloudinary.com/rafamed-dev/image/upload/v1743211572/cisef/hero2_xaatek.jpg',
// ];

interface CarouselProps {
  carouselItems: string[];
}

const { carouselItems: items } = defineProps<CarouselProps>();

const carouselRef = ref();

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return;

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0);
    }

    carouselRef.value.next();
  }, 3000);
});
</script>

<template>
  <UCarousel
    ref="carouselRef"
    v-slot="{ item }"
    :items="items"
    :ui="{ item: 'basis-full' }"
    class="rounded-lg overflow-hidden"
    indicators
  >
    <img :src="item" class="w-full" draggable="false" />
  </UCarousel>
</template>
