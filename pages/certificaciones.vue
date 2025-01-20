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

useSeoMeta({
  title: 'Certificaciones y reconocimientos | CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description: 'Certificaciones y reconocimientos de CISEF',
  ogDescription: 'Certificaciones y reconocimientos de CISEF',
  ogImage: '',
  ogTitle: 'Certificaciones y reconocimientos | CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer>
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Cerficaciones y reconocimientos</h1>

      <p class="text-xl mt-4">Reconocimientos que respaldan nuestra calidad y confiabilidad</p>
    </section>

    <div class="relative py-12 h-full">
      <section class="grid grid-cols-1 gap-8">
        <UCard
          :ui="{
            background: 'bg-gradient-to-br from-blue-100 to-green-100',
            shadow: 'shadow-pinterest',
          }"
        >
          <template #header>
            <h3 class="md:text-3xl text-xl font-bold">Certificados nacionales e internacionales</h3>
          </template>

          <section class="flex flex-col md:flex-row md:justify-between gap-12 md:py-12 md:px-6">
            <div class="">
              <h4 class="font-bold text-primary text-center">SADER</h4>
              <ul class="flex flex-col gap-8 pt-4">
                <li class="flex items-center gap-2">
                  <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                  <section class="flex flex-col">
                    <span class="font-bold text-xl">Bacteriología:</span>
                    <span>LAB-260324-07-BACT-003</span>
                  </section>
                </li>
                <li class="flex items-center gap-2">
                  <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                  <section class="flex flex-col">
                    <span class="font-bold text-xl">Micología:</span>
                    <span>LAB-260324-07-MICO-003</span>
                  </section>
                </li>
                <li class="flex items-center gap-2">
                  <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                  <section class="flex flex-col">
                    <span class="font-bold text-xl">Entomología:</span>
                    <span>LAB-260324-07-ENTO-003</span>
                  </section>
                </li>
              </ul>
            </div>
            <div class="">
              <h4 class="font-bold text-primary text-center">EMA</h4>
              <ul class="flex flex-col gap-8 pt-4">
                <li class="flex items-center gap-2">
                  <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                  <section class="flex flex-col">
                    <span class="font-bold text-xl">Sanidad agropecuaria:</span>
                    <span>SA-096-006/09</span>
                  </section>
                </li>
                <li class="flex items-center gap-2">
                  <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                  <section class="flex flex-col">
                    <span class="font-bold text-xl">Alimentos:</span>
                    <span>A-1512-136/22</span>
                  </section>
                </li>
              </ul>
            </div>
            <section class="flex flex-col md:items-center gap-2">
              <h4 class="text-center font-bold text-primary">INTERNACIONALES</h4>
              <span class="flex items-center gap-2"
                ><Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                NMX-EC-17025-IMNC-2018</span
              >
            </section>
          </section>
        </UCard>
      </section>
    </div>
  </UContainer>
</template>
