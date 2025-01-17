<script setup lang="ts">
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
    <section class="pt-12">
      <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">Sobre nosotros</h1>
      <p class="text-xl mt-4">Conoce más sobre CISEF</p>
    </section>

    <section class="md:py-12">
      <section class="flex flex-col md:flex-row justify-between mt-8 gap-8">
        <UCard
          class="md:w-1/2"
          :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }"
        >
          <div class="flex flex-col gap-8">
            <section class="flex flex-col gap-2">
              <h3 class="text-2xl font-bold">Misión</h3>
              <p class="font-light">
                Ser una empresa líder en el mercado de servicios de diagnóstico fitosanitario, con calidad y tecnología
                de vanguardia, que contribuya al desarrollo sustentable de la agricultura.
              </p>
            </section>
            <section class="flex flex-col gap-2">
              <h3 class="text-2xl font-bold">Visión</h3>
              <p class="font-light">
                Ser una empresa líder en el mercado de servicios de diagnóstico fitosanitario, con calidad y tecnología
                de vanguardia, que contribuya al desarrollo sustentable de la agricultura.
              </p>
            </section>
            <section class="flex flex-col gap-2">
              <h3 class="text-2xl font-bold">Valores</h3>
              <p class="font-light">
                Calidad, ética, responsabilidad, compromiso, innovación, trabajo en equipo, respeto, honestidad,
                lealtad, profesionalismo.
              </p>
            </section>
          </div>
        </UCard>
        <UCard
          class="md:w-1/2 overflow-hidden min-h-full"
          :ui="{
            background: 'bg-gradient-to-br from-blue-100 to-green-100',
            body: { padding: '' },
            shadow: 'shadow-pinterest',
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
                src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=Francisco%20de+%20Urdi%C3%B1ola%20No.%20360,%20Saltillo,%20Coahuila,%20M%C3%A9xico.%20C.P.%2025000.+(CISEF)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
              ></iframe>
            </div>
          </ClientOnly>
        </UCard>
      </section>
    </section>
  </UContainer>
</template>
