<script setup lang="ts">
import { Motion } from 'motion-v';

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

const sectors = [
  'Agricultores',
  'Sociedades de producción rural',
  'Empresas procesadoras de alimentos',
  'Empresas orientadas a la industria de semillas',
  'Importadores del sector agrícola y pecuario',
  'Industria de los agroquímicos',
];

useSeoMeta({
  title: 'CISEF - Centro de Investigación y Servicios en Fitosanidad',
  description:
    'Brindamos servicios de diagnóstico confiables para el manejo eficiente de plagas y la calidad agroalimentaria.',
  ogDescription: 'CISEF - Centro de Investigación y Servicios en Fitosanidad',
  ogImage: '',
  ogTitle: 'CISEF - Centro de Investigación y Servicios en Fitosanidad',
});
</script>

<template>
  <UContainer>
    <section class="flex gap-8 md:gap-16 flex-col md:flex-row justify-between items-center min-h-[70vh] py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :animate="{ x: 0, opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        class="flex flex-col gap-4 md:gap-8 md:basis-3/5"
        as="section"
      >
        <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">
          Comprometidos con la sanidad vegetal y la seguridad agroalimentaria
        </h1>
        <p class="text-lg md:text-xl">
          Brindamos servicios de diagnóstico confiables para el manejo eficiente de plagas y la calidad agroalimentaria.
        </p>

        <Motion
          :initial="{
            opacity: 0,
          }"
          :animate="{ opacity: 1 }"
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.5 }"
          class="flex gap-4"
          as="section"
        >
          <UButton to="/servicios" color="green" variant="outline" size="lg" icon="i-heroicons-arrow-small-right"
            >Nuestros servicios</UButton
          >
          <UButton to="/contacto" color="green" size="lg" icon="i-heroicons-phone-arrow-down-left">Contáctanos</UButton>
        </Motion>
      </Motion>
      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :animate="{ y: 0, opacity: 1 }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
      >
        <figure class="basis-2/5">
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/Valores_gti5x1.png"
            alt=""
            class="w-full"
          />
        </figure>
      </Motion>
    </section>

    <UDivider />

    <section class="py-12 flex flex-col md:flex-row justify-between gap-8 items-center">
      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="md:w-1/3 h-full rounded-xl overflow-hidden shadow-pinterest"
        as="figure"
      >
        <img src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/hero_vbzg9x.jpg" alt="" />
      </Motion>
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        class="md:w-1/2"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Sobre CISEF</h2>
        <p class="text-xl mt-4">
          Desde 1997, somos un laboratorio certificado por SADER que contribuye al manejo sostenible de plagas agrícolas
          y a la calidad agroalimentaria.
        </p>
        <Motion
          :initial="{
            opacity: 0,
          }"
          :in-view="{ opacity: 1 }"
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.7 }"
          class="mt-8"
          as="section"
        >
          <UButton to="/sobre-nosotros" color="green" size="lg" icon="i-heroicons-arrow-small-right"
            >Conoce más sobre nosotros</UButton
          >
        </Motion>
      </Motion>
    </section>

    <UDivider />

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Nuestros servicios</h2>
        <p class="text-xl mt-4">Diagnósticos especializados para la sanidad y calidad agroalimentaria.</p>
      </Motion>
      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8"
        as="section"
      >
        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <section class="z-10 relative">
            <h3 class="text-3xl font-bold text-gray-50">Fitosanidad</h3>
            <p class="text-gray-100 font-light">
              Diagnósticos precisos en virus, bacterias, hongos, nematodos, malezas e insectos para proteger tus
              cultivos.
            </p>
          </section>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/fitosanidad_i6vtui.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>

        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <section class="z-10 relative">
            <h3 class="text-3xl font-bold text-gray-50">Inocuidad Agroalimentaria</h3>
            <p class="text-gray-100 font-light">
              Análisis microbiológicos que garantizan la seguridad y calidad de tus productos agroalimentarios.
            </p>
          </section>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/inocuidad_nawkiy.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>

        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <section class="z-10 relative">
            <h3 class="text-3xl font-bold text-gray-50">Sanidad Acuícola y Pesquera</h3>
            <p class="text-gray-100 font-light">
              Análisis microbiológicos que garantizan la seguridad y calidad de tus productos agroalimentarios.
            </p>
          </section>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/acuicola_wjnbar.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>

        <UCard class="relative overflow-hidden h-96 grid place-content-center p-2">
          <section class="z-10 relative">
            <h3 class="text-3xl font-bold text-gray-50">Calidad de la Semilla</h3>
            <p class="text-gray-100 font-light">
              Evaluamos la viabilidad y pureza de las semillas para asegurar cultivos de alto rendimiento.
            </p>
          </section>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539670/cisef/semilla_g6s7u1.jpg"
            alt=""
            class="absolute inset-0 z-0 brightness-50 h-full object-cover w-full"
          />
        </UCard>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
        }"
        :in-view="{ opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.7 }"
        class="flex justify-center mt-8"
        as="section"
      >
        <UButton to="/servicios" color="green" size="lg" icon="i-heroicons-arrow-small-right"
          >Conoce más sobre nuestros servicios</UButton
        >
      </Motion>
    </section>

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">¿Por qué elegir CISEF?</h2>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
      >
        <section class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8">
          <UCard :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }">
            <section class="flex flex-col gap-8 py-12">
              <Icon name="hugeicons:certificate-01" size="64" class="text-green-500" />
              <span class="text-2xl">Reconocimientos nacionales e internacionales</span>
            </section>
          </UCard>

          <UCard :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }">
            <section class="flex flex-col gap-8 py-12">
              <Icon name="hugeicons:dashboard-speed-01" size="64" class="text-green-500" />
              <span class="text-2xl">Resultados confiables y rápidos</span>
            </section>
          </UCard>

          <UCard :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }">
            <section class="flex flex-col gap-8 py-12">
              <Icon name="hugeicons:user-check-01" size="64" class="text-green-500" />
              <span class="text-2xl">Personal calificado y tecnología de vanguardia</span>
            </section>
          </UCard>
          <UCard :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }">
            <section class="flex flex-col gap-8 py-12">
              <Icon name="hugeicons:checkmark-square-03" size="64" class="text-green-500" />
              <span class="text-2xl">Transparencia e imparcialidad en los diagnósticos</span>
            </section>
          </UCard>
        </section>
      </Motion>
    </section>

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        as="section"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Sectores atendidos</h2>
        <p class="text-xl mt-4">Soluciones específicas para cada área del sector agroalimentario</p>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
      >
        <section class="flex justify-between items-center gap-8 py-12">
          <UCard
            :ui="{
              background: '',
              ring: '',
              shadow: '',
              base: 'w-1/2 h-full min-h-full',
              body: { padding: '' },
            }"
          >
            <p class="md:text-3xl text-xl leading-snug italic">
              En <span class="font-bold text-primary">CISEF</span>, entendemos las necesidades únicas de cada sector
              dentro de la cadena agroalimentaria.
            </p>
          </UCard>
          <figure class="w-1/2 grid md:grid-cols-2 rounded-xl overflow-hidden h-full min-h-full">
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/fitosanidad_i6vtui.jpg"
              alt=""
              class="object-cover min-h-full"
            />
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/inocuidad_nawkiy.jpg"
              alt=""
              class="object-cover min-h-full"
            />
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/acuicola_wjnbar.jpg"
              alt=""
              class="object-cover min-h-full"
            />
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539670/cisef/semilla_g6s7u1.jpg"
              alt=""
              class="object-cover min-h-full"
            />
          </figure>
        </section>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
      >
        <p class="text-2xl text-primary font-bold mt-4">Nuestros servicios están dirigidos a:</p>
      </Motion>

      <section class="flex flex-col md:flex-row md:justify-between md:items-center gap-8 py-12">
        <Motion
          :initial="{
            opacity: 0,
            y: -150,
          }"
          :in-view="{ y: 0, opacity: 1 }"
          :in-view-options="{ amount: 'all', once: true }"
          :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
          class="md:w-1/2 grid grid-cols-2 rounded-xl overflow-hidden h-full min-h-full"
          as="figure"
        >
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/fitosanidad_i6vtui.jpg"
            alt=""
            class="object-cover min-h-full"
          />
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/inocuidad_nawkiy.jpg"
            alt=""
            class="object-cover min-h-full"
          />
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/acuicola_wjnbar.jpg"
            alt=""
            class="object-cover min-h-full"
          />
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539670/cisef/semilla_g6s7u1.jpg"
            alt=""
            class="object-cover min-h-full"
          />
        </Motion>
        <Motion
          :initial="{
            opacity: 0,
            x: -100,
          }"
          :in-view="{ x: 0, opacity: 1 }"
          :in-view-options="{ amount: 'all', once: true }"
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
          class="md:w-1/2 h-full min-h-full"
        >
          <UCard
            :ui="{
              background: '',
              ring: '',
              shadow: '',

              body: { padding: '' },
            }"
          >
            <ul class="flex flex-col gap-8">
              <li v-for="(sector, index) in sectors" :key="sector" class="flex items-center gap-2 md:gap-4">
                <div class="shrink-0">
                  <Icon name="i-heroicons-check-circle" size="32" class="text-green-500" />
                </div>
                <span class="text-xl">{{ sector }}</span>
              </li>
            </ul>
          </UCard>
        </Motion>
      </section>
    </section>

    <section class="md:py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        as="section"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Nuestras Certificaciones</h2>
        <p class="text-xl mt-4">Reconocimientos que respaldan nuestra calidad y confiabilidad</p>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="relative py-12 h-full"
        as="section"
      >
        <section class="grid grid-cols-1 gap-8">
          <UCard
            :ui="{
              background: 'bg-gradient-to-br from-blue-100 to-green-100',
              shadow: 'shadow-pinterest',
              base: 'max-w-3xl mx-auto',
            }"
          >
            <template #header>
              <h3 class="md:text-3xl text-xl font-bold">Certificados nacionales e internacionales</h3>
            </template>

            <section class="flex flex-col md:flex-row md:justify-between gap-12">
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
            </section>
            <section class="flex flex-col md:items-center gap-2 pt-12 md:pt-8">
              <h4 class="text-center font-bold text-primary">INTERNACIONALES</h4>
              <span class="flex items-center gap-2"
                ><Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                NMX-EC-17025-IMNC-2018</span
              >
            </section>
          </UCard>
        </section>
        <Motion
          :initial="{
            opacity: 0,
          }"
          :in-view="{ opacity: 1 }"
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.7 }"
          class="mt-8 flex justify-center"
          as="section"
        >
          <UButton to="/certificaciones" color="green" icon="i-heroicons-arrow-small-right" size="lg"
            >Ver todas las certificaciones</UButton
          >
        </Motion>
      </Motion>
    </section>

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -100,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        as="section"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Contáctanos</h2>
      </Motion>
      <Motion
        :initial="{
          opacity: 0,
          y: -150,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="flex flex-col md:flex-row justify-between mt-8 gap-8"
        as="section"
      >
        <UCard
          class="md:w-1/2"
          :ui="{ background: 'bg-gradient-to-br from-blue-100 to-green-100', shadow: 'shadow-pinterest' }"
        >
          <div class="flex flex-col gap-8">
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
                src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=Francisco%20de%20Urdi%C3%B1ola%20No.%20360,%20Saltillo,%20Coahuila,%20M%C3%A9xico.%20C.P.%2025000.+(CISEF)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
              ></iframe>
            </div>
          </ClientOnly>
        </UCard>
      </Motion>
      <Motion
        :initial="{
          opacity: 0,
        }"
        :in-view="{ opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.7 }"
        class="mt-8 flex justify-center"
        as="section"
      >
        <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
      </Motion>
    </section>
  </UContainer>
</template>
