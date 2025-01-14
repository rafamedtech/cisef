<script setup lang="ts">
const certificates = [
  {
    id: 1,
    title: 'ISO 9001:2015',
    description: 'Certificación de calidad en la prestación de servicios de diagnóstico fitosanitario.',
    image: '',
  },
  {
    id: 2,
    title: 'ISO 17025:2017',
    description: 'Certificación de calidad en la prestación de servicios de diagnóstico fitosanitario.',
    image: '',
  },
  {
    id: 3,
    title: 'ISO 14001:2015',
    description: 'Certificación de calidad en la prestación de servicios de diagnóstico fitosanitario.',
    image: '',
  },
  {
    id: 4,
    title: 'ISO 45001:2018',
    description: 'Certificación de calidad en la prestación de servicios de diagnóstico fitosanitario.',
    image: '',
  },
];
</script>

<template>
  <UContainer>
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Cerficaciones y reconocimientos</h1>
    </section>

    <div class="relative py-12 h-full">
      <section class="absolute inset-0 flex justify-center items-center z-50">
        <UButton size="lg" color="gray"><span class="text-5xl">Sección en construcción</span></UButton>
      </section>
      <section class="grid grid-cols-1 md:grid-cols-4 gap-8 blur-sm">
        <CertCard
          v-for="cert in certificates"
          :key="cert.id"
          :title="cert.title"
          :description="cert.description"
          :image="cert.image"
        />
      </section>
    </div>
  </UContainer>
</template>
