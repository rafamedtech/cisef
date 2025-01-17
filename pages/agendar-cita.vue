<script setup lang="ts">
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
      <p class="text-xl mt-4">Da el primer paso para que empecemos a trabajar juntos</p>
    </section>

    <section class="pt-12 md:pt-24 pb-12 flex flex-col-reverse md:flex-row gap-8 justify-between">
      <UCard class="basis-2/5">
        <UForm :state="fields">
          <div class="flex flex-col gap-4">
            <UFormGroup label="Nombre" size="lg" :ui="{ label: { base: 'text-lg' } }">
              <UInput placeholder="Escribe aquí" />
            </UFormGroup>
            <UFormGroup label="Teléfono" size="lg" :ui="{ label: { base: 'text-lg' } }">
              <UInput placeholder="Escribe aquí" />
            </UFormGroup>
            <UFormGroup label="Correo electrónico" size="lg" :ui="{ label: { base: 'text-lg' } }">
              <UInput placeholder="Escribe aquí" />
            </UFormGroup>
            <UFormGroup label="Empresa" size="lg" :ui="{ label: { base: 'text-lg' } }">
              <UInput placeholder="Escribe aquí" />
            </UFormGroup>
          </div>

          <section class="pt-6 flex justify-end">
            <UButton color="green" icon="i-heroicons-envelope" size="lg">Enviar</UButton>
          </section>
        </UForm>
      </UCard>
      <figure class="basis-2/5 pb-8 md:pb-0">
        <img
          src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/Valores_gti5x1.png"
          alt=""
          class="w-full"
        />
      </figure>
    </section>
  </UContainer>
</template>
