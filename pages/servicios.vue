<script setup lang="ts">
const services = [
  {
    id: 1,
    title: 'Fitosanidad',
    description:
      'Diagnósticos precisos en virus, bacterias, hongos, nematodos, malezas e insectos para proteger tus cultivos.',
    image: 'https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/fitosanidad_i6vtui.jpg',
  },
  {
    id: 2,
    title: 'Inocuidad Agroalimentaria',
    description: 'Análisis microbiológicos que garantizan la seguridad y calidad de tus productos agroalimentarios.',
    image: 'https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/inocuidad_nawkiy.jpg',
  },
  {
    id: 3,
    title: 'Sanidad Acuícola y Pesquera',
    description: 'Análisis microbiológicos que garantizan la seguridad y calidad de tus productos agroalimentarios.',
    image: 'https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/acuicola_wjnbar.jpg',
  },
  {
    id: 4,
    title: 'Calidad de la Semilla',
    description: 'Evaluamos la viabilidad y pureza de las semillas para asegurar cultivos de alto rendimiento.',
    image: 'https://res.cloudinary.com/rafamed-dev/image/upload/v1736539670/cisef/semilla_g6s7u1.jpg',
  },
];

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

    <section class="grid grid-cols-1 md:grid-cols-2 gap-8 mt-8">
      <ServiceCard
        v-for="service in services"
        :key="service.id"
        :title="service.title"
        :description="service.description"
        :image="service.image"
      />
    </section>

    <section class="flex justify-center py-8">
      <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
    </section>
  </UContainer>
</template>
