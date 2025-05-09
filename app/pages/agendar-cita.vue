<script setup lang="ts">
import { Motion } from 'motion-v';
import { variants } from '@/lib/animations';

const { container, moveUp } = variants;
const fields = ref({
  name: '',
  email: '',
  phone: '',
  message: '',
});

useSeoMeta({
  title: 'Agendar una cita | CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description: 'Agenda una cita con nosotros',
  ogDescription: 'Agenda una cita con nosotros',
  ogImage: '',
  ogTitle: 'Agendar una cita | CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer class="min-h-full pb-12">
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Agenda una cita con nosotros</h1>
      <p class="text-xl mt-4 dark:text-black">Da el primer paso para que empecemos a trabajar juntos</p>
    </section>

    <Motion
      as="section"
      class="pt-12 md:pt-24 pb-12 flex flex-col-reverse md:flex-row items-center gap-8 justify-between"
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
      <Motion :variants="moveUp" as="figure" class="md:h-[30rem] h-full rounded-lg overflow-hidden shadow-pinterest">
        <img
          src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743459188/cisef/customer_lou9at.jpg"
          alt=""
          class="w-full h-full"
        />
      </Motion>
      <Motion :variants="moveUp" class="md:basis-2/5 w-full shadow-pinterest h-full">
        <UCard :ui="{ background: 'dark:bg-gray-100', ring: 'dark:ring-gray-200' }">
          <UForm :state="fields">
            <div class="flex flex-col gap-4">
              <UFormGroup label="Nombre" size="xl" :ui="{ label: { base: 'text-lg dark:text-gray-700' } }">
                <UInput
                  placeholder="Escribe aquí"
                  :ui="{ color: { white: { outline: 'dark:bg-white dark:ring-gray-300' } } }"
                />
              </UFormGroup>
              <UFormGroup label="Teléfono" size="xl" :ui="{ label: { base: 'text-lg dark:text-gray-700' } }">
                <UInput
                  placeholder="Escribe aquí"
                  :ui="{ color: { white: { outline: 'dark:bg-white dark:ring-gray-300' } } }"
                />
              </UFormGroup>
              <UFormGroup label="Correo electrónico" size="xl" :ui="{ label: { base: 'text-lg dark:text-gray-700' } }">
                <UInput
                  placeholder="Escribe aquí"
                  :ui="{ color: { white: { outline: 'dark:bg-white dark:ring-gray-300' } } }"
                />
              </UFormGroup>
              <UFormGroup label="Empresa" size="xl" :ui="{ label: { base: 'text-lg dark:text-gray-700' } }">
                <UInput
                  placeholder="Escribe aquí"
                  :ui="{ color: { white: { outline: 'dark:bg-white dark:ring-gray-300' } } }"
                />
              </UFormGroup>
            </div>

            <section class="pt-6 flex justify-end">
              <UButton color="green" icon="i-heroicons-envelope" size="lg">Enviar</UButton>
            </section>
          </UForm>
        </UCard>
      </Motion>
    </Motion>
  </UContainer>
</template>
