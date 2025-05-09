<script setup lang="ts">
import { Motion } from 'motion-v';
import { carouselItems } from '@/lib/pageData';
import { variants } from '@/lib/animations';

const { container, moveUp } = variants;

useSeoMeta({
  title: 'Sobre nosotros | CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description: 'Conoce más sobre CISEF',
  ogDescription: 'Conoce más sobre CISEF',
  ogImage: '',
  ogTitle: 'Sobre nosotros | CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer>
    <!-- Encabezado -->
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Sobre CISEF</h1>
      <p class="text-xl mt-4 dark:text-black">
        Comprometidos con la sanidad vegetal y la calidad agroalimentaria desde 1997
      </p>
    </section>

    <section class="py-10">
      <Motion :variants="moveUp" initial="hidden" animate="visible" :transition="{ delay: 0.2 }">
        <Carousel class="md:hidden" :carouselItems="carouselItems" />
      </Motion>
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
        class="hidden md:flex gap-4"
      >
        <Motion :variants="moveUp" v-for="item in carouselItems">
          <figure class="flex gap-4 justify-center">
            <img :src="item" class="rounded-lg shadow-lg" />
          </figure>
        </Motion>
      </Motion>
    </section>

    <!-- Introducción -->
    <section class="mx-auto md:py-10 pb-10">
      <p class="text-lg leading-relaxed dark:text-black">
        El Centro Internacional de Servicios Fitosanitarios (CISEF) es un laboratorio de diagnóstico certificado que
        brinda soluciones innovadoras para el sector agroalimentario. Desde nuestra fundación en 1997, hemos trabajado
        para garantizar la sanidad vegetal, animal y humana, respaldados por normas nacionales e internacionales.
      </p>
    </section>

    <!-- Historia y Origen -->
    <section class="md:py-10">
      <div class="mx-auto">
        <h2 class="text-2xl font-bold text-primary">Nuestra Historia</h2>
        <p class="mt-4 text-lg leading-relaxed dark:text-black">
          Fundado en febrero de 1997, CISEF nació con el objetivo de atender la creciente necesidad de diagnósticos
          confiables en el sector agrícola. Estamos estratégicamente ubicados en Saltillo, Coahuila, una región clave
          para la producción agrícola en México, y colaboramos activamente con SADER para ofrecer servicios de alta
          calidad respaldados por acreditaciones nacionales e internacionales.
        </p>
      </div>
    </section>

    <!-- Misión, Visión y Valores -->
    <section class="md:py-10 pt-8 w-full">
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
        class="flex flex-col md:flex-row items-center gap-12"
      >
        <Motion :variants="moveUp">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
            }"
            class="md:basis-1/2"
          >
            <section class="flex flex-col gap-8 py-8 px-6">
              <section>
                <h2 class="text-2xl font-bold text-primary">Misión</h2>
                <p class="mt-4 text-lg leading-relaxed dark:text-black">
                  Evaluar la calidad agroalimentaria y detectar oportunamente patógenos para apoyar la toma de
                  decisiones de nuestros clientes y autoridades nacionales e internacionales.
                </p>
              </section>

              <section>
                <h2 class="text-2xl font-bold text-primary">Visión</h2>
                <p class="mt-4 text-lg leading-relaxed dark:text-black">
                  Ser una empresa de vanguardia reconocida por mantener e incrementar acreditaciones nacionales e
                  internacionales, promoviendo la seguridad humana, la calidad y la protección al medio ambiente.
                </p>
              </section>
            </section>
          </UCard>
        </Motion>

        <Motion :variants="moveUp" class="md:basis-1/2 w-full h-full">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
            }"
            class="w-full"
          >
            <section class="py-8 px-6">
              <h2 class="text-2xl font-bold text-primary">Valores</h2>
              <ul class="mt-4 text-lg grid list-disc list-inside gap-2 dark:text-black">
                <li>Responsabilidad</li>
                <li>Vanguardia</li>
                <li>Confidencialidad</li>
                <li>Profesionalismo</li>
                <li>Liderazgo</li>
                <li>Honestidad</li>
                <li>Trabajo en equipo</li>
                <li>Crecimiento constante</li>
              </ul>
            </section>
          </UCard>
        </Motion>
      </Motion>
    </section>

    <!-- Reconocimientos y Certificaciones -->
    <section class="py-10">
      <div class="mx-auto">
        <h2 class="text-2xl font-bold text-primary">Reconocimientos y Certificaciones</h2>
        <p class="mt-4 text-lg leading-relaxed dark:text-black">
          Contamos con acreditaciones como NMX-EC-17025-IMNC-2018 y las cédulas de SADER, que respaldan la calidad y
          confiabilidad de nuestros diagnósticos.
        </p>
        <section class="flex justify-center pt-8">
          <UButton to="/certificaciones" color="green" icon="i-heroicons-arrow-small-right" size="lg"
            >Ver todas las certificaciones</UButton
          >
        </section>
      </div>
    </section>
  </UContainer>
</template>
