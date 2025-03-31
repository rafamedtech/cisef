<script setup lang="ts">
import { Motion } from 'motion-v';
import { variants } from '@/lib/animations';
import { services } from '@/lib/pageData';

const { container, moveUp } = variants;

useSeoMeta({
  title: 'Nuestros servicios | CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description: 'Conoce los servicios que ofrecemos en CISEF',
  ogDescription: 'Conoce los servicios que ofrecemos en CISEF',
  ogImage: '',
  ogTitle: 'Nuestros servicios | CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer>
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Conoce nuestros servicios</h1>
      <p class="text-lg md:text-xl text-gray-600 mt-4">
        Diagnósticos especializados para la sanidad y calidad agroalimentaria.
      </p>
    </section>

    <Motion
      as="ul"
      :variants="container"
      initial="hidden"
      animate="visible"
      :transition="{
        type: 'spring',
        delayChildren: 0.3,
        staggerChildren: 0.2,
      }"
      class="grid grid-cols-1 md:grid-cols-4 md:gap-8 pt-8"
    >
      <Motion :variants="moveUp" class="flex gap-4 py-8" as="section" v-for="service in services">
        <ServiceCard
          :key="service.id"
          :title="service.title"
          :description="service.description"
          :image="service.image"
        />
      </Motion>
    </Motion>

    <section class="flex justify-center py-8">
      <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
    </section>
  </UContainer>
</template>
