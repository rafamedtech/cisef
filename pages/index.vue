<script setup lang="ts"></script>

<template>
  <UContainer>
    <section class="flex gap-8 md:gap-16 flex-col md:flex-row justify-between items-center min-h-[70vh] py-12">
      <section class="flex flex-col gap-4 md:gap-8 md:basis-3/5">
        <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">
          Comprometidos con la sanidad vegetal y la seguridad agroalimentaria
        </h1>
        <p class="text-lg md:text-xl">
          Brindamos servicios de diagnóstico confiables para el manejo eficiente de plagas y la calidad agroalimentaria.
        </p>
        <section class="flex gap-4">
          <UButton to="/" color="green" variant="outline" size="lg" icon="i-heroicons-arrow-small-right"
            >Nuestros servicios</UButton
          >
          <UButton to="/" color="green" size="lg" icon="i-heroicons-phone-arrow-down-left">Contáctanos</UButton>
        </section>
      </section>
      <figure class="basis-2/5">
        <img src="@/assets/images/valores.png" alt="" class="w-full" />
      </figure>
    </section>

    <UDivider />

    <section class="py-12 flex justify-between gap-8 items-center">
      <figure class="w-1/3 h-full rounded-xl overflow-hidden">
        <img src="@/assets/images/hero.jpg" alt="" />
      </figure>
      <div class="w-1/2">
        <h2 class="text-5xl font-semibold text-primary">Sobre CISEF</h2>
        <p class="text-xl mt-4">
          Desde 1997, somos un laboratorio certificado por SADER que contribuye al manejo sostenible de plagas agrícolas
          y a la calidad agroalimentaria.
        </p>
      </div>
    </section>

    <UDivider />

    <section class="py-12">
      <h2 class="text-5xl font-semibold text-primary text-center">Nuestros servicios</h2>
      <p class="text-xl text-center mt-4">Diagnósticos especializados para la sanidad y calidad agroalimentaria.</p>
      <section class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8">
        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <h3 class="text-3xl font-semibold text-gray-100 z-10 relative">Fitosanidad</h3>
          <img
            src="@/assets/images/fitosanidad.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>
        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <h3 class="text-3xl font-semibold text-gray-100 z-10 relative">Inocuidad Agroalimentaria</h3>
          <img
            src="@/assets/images/inocuidad.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>
        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <h3 class="text-3xl font-semibold text-gray-100 z-10 relative">Sanidad Acuícola y Pesquera</h3>
          <img
            src="@/assets/images/acuicola.png"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>
        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <h3 class="text-3xl font-semibold text-gray-100 z-10 relative">Calidad de la Semilla</h3>
          <img
            src="@/assets/images/semilla.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>
      </section>

      <section class="flex justify-center mt-8">
        <UButton to="/" color="green" size="lg" icon="i-heroicons-arrow-small-right"
          >Conoce más sobre nuestros servicios</UButton
        >
      </section>
    </section>

    <section>
      <h2 class="text-5xl font-semibold text-primary text-center">Certificaciones</h2>
      <p class="text-xl text-center mt-4">Algunas de nuestras certificaciones</p>
    </section>
  </UContainer>
</template>
