<script setup lang="ts">
import { Motion } from 'motion-v';
import { variants } from '@/lib/animations';

const { container, moveUp } = variants;

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

      <p class="text-xl mt-4 dark:text-black">Reconocimientos que respaldan nuestra calidad y confiabilidad</p>
    </section>

    <div class="relative py-12 h-full">
      <Motion
        :variants="container"
        as="section"
        initial="hidden"
        in-view="visible"
        :in-view-options="{ amount: 'some', once: true }"
        :transition="{
          type: 'spring',
          delayChildren: 0.3,
          staggerChildren: 0.2,
        }"
        class="flex flex-col md:flex-row md:justify-between gap-8 md:py-12"
      >
        <Motion :variants="moveUp">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
              divide: 'dark:divide-gray-200',
            }"
            class="md:h-96"
          >
            <template #header>
              <h4 class="font-bold text-primary text-center">SADER</h4>
            </template>
            <ul class="flex flex-col gap-8 pt-4 dark:text-black justify-center">
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
          </UCard>
        </Motion>
        <Motion :variants="moveUp">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
              divide: 'dark:divide-gray-200',
            }"
            class="md:h-96"
          >
            <template #header>
              <h4 class="font-bold text-primary text-center">EMA</h4>
            </template>
            <ul class="flex flex-col gap-8 pt-4 dark:text-black justify-center">
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
          </UCard>
        </Motion>
        <Motion :variants="moveUp">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
              divide: 'dark:divide-gray-200',
            }"
            class="md:h-96"
          >
            <template #header>
              <h4 class="text-center font-bold text-primary">INTERNACIONALES</h4>
            </template>
            <section class="flex flex-col md:items-center gap-2">
              <span class="flex items-center gap-2 dark:text-black"
                ><Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                NMX-EC-17025-IMNC-2018</span
              >
            </section>
          </UCard>
        </Motion>
      </Motion>
    </div>
  </UContainer>
</template>
