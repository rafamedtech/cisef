<script setup lang="ts">
import { Motion } from 'motion-v';
import { variants } from '@/lib/animations';

const { container, moveUp } = variants;

useSeoMeta({
  title: 'Contacto | CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description: 'Contacta a CISEF',
  ogDescription: 'Contacta a CISEF',
  ogImage: '',
  ogTitle: 'Contacto | CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer class="min-h-full pb-12">
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Contáctanos</h1>
      <p class="text-xl mt-4 dark:text-black">Conoce nuestra información de contacto</p>
    </section>

    <section class="md:py-12">
      <Motion
        as="section"
        class="flex flex-col md:flex-row justify-between mt-8 gap-8"
        :variants="container"
        initial="hidden"
        in-view="visible"
        :in-view-options="{ amount: 'some', once: true }"
        :transition="{
          type: 'spring',
          delayChildren: 0.3,
          staggerChildren: 0.2,
        }"
      >
        <Motion :variants="moveUp" class="md:w-1/2">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
            }"
          >
            <div class="flex flex-col gap-8 dark:text-black">
              <section class="flex flex-col gap-2">
                <h3 class="text-2xl font-bold">Dirección</h3>
                <p class="font-light">Francisco de Urdiñola No. 360, Saltillo, Coahuila, México. C.P. 25000.</p>
              </section>
              <section class="flex flex-col gap-2">
                <h3 class="text-2xl font-bold">Teléfonos y correo electrónico</h3>
                <p class="font-light">Tel.: (844) 4-12-37-56, (844) 4-12-37-92, (844) 4-10-51-76</p>
                <p class="font-light">Lada sin costo: 01 800 714 99 79</p>
                <p class="font-light">Correo: atencion.aclientes@ciseflab.com.mx</p>
              </section>
              <section class="flex flex-col gap-2">
                <h3 class="text-2xl font-bold">Horario de atención</h3>
                <p class="font-light">Lunes a viernes: 7:00 a.m. a 7:00 p.m.</p>
                <p class="font-light">Sábados, domingos y días festivos: Según carga de trabajo</p>
              </section>
            </div>
          </UCard>
        </Motion>
        <Motion :variants="moveUp" class="md:w-1/2 overflow-hidden min-h-full">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              body: { padding: '' },
              shadow: 'shadow-pinterest',
              ring: 'dark:ring-gray-200',
            }"
          >
            <ClientOnly>
              <div class="w-full min-h-full h-full">
                <iframe
                  width="100%"
                  height="400px"
                  frameborder="0"
                  scrolling="no"
                  marginheight="0"
                  marginwidth="0"
                  src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=Francisco%20de%20Urdi%C3%B1ola%20No.%20360,%20Saltillo,%20Coahuila,%20M%C3%A9xico.%20C.P.%2025000.+(CISEF)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
                ></iframe>
              </div>
            </ClientOnly>
          </UCard>
        </Motion>
      </Motion>
      <section class="mt-8 flex justify-center">
        <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
      </section>
    </section>
  </UContainer>
</template>
