<script setup lang="ts">
import { Motion } from 'motion-v';
import { sectors, services, benefits } from '@/lib/pageData';
import { variants } from '@/lib/animations';

const { container, moveUp: items, moveRight } = variants;

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
    <section class="flex gap-8 md:gap-16 flex-col-reverse md:flex-row justify-between items-center min-h-[70vh] py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -30,
        }"
        :animate="{ x: 0, opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        class="flex flex-col gap-4 md:gap-8 md:basis-3/5"
        as="section"
      >
        <h1 class="text-4xl md:text-6xl font-semibold text-primary leading-tight">
          Comprometidos con la sanidad vegetal y la seguridad agroalimentaria
        </h1>
        <p class="text-lg md:text-xl dark:text-black">
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
      <!-- <Motion
        :initial="{
          opacity: 0,
          y: 20,
        }"
        :animate="{ y: 0, opacity: 1 }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
      >
         <figure class="basis-2/5 relative">
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743207100/cisef/hero1_apnbpu.jpg"
            alt=""
            class="h-[30rem] object-cover rounded-2xl shadow-lg"
          />
        </figure> 
      </Motion> -->

      <HeroCarousel />
    </section>

    <UDivider :ui="{ border: { base: 'dark:border-gray-200' } }" />

    <section class="py-12 flex flex-col md:flex-row justify-between gap-8 items-center">
      <Motion
        :initial="{
          opacity: 0,
          y: 20,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 } }"
        class="md:w-1/3 h-full rounded-xl overflow-hidden shadow-pinterest"
        as="figure"
      >
        <img src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743207100/cisef/hero2_tdva24.jpg" alt="" />
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          x: -30,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        class="md:w-1/2"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Sobre CISEF</h2>
        <p class="text-xl mt-4 dark:text-black">
          Desde 1997, somos un laboratorio certificado por SADER que contribuye al manejo sostenible de plagas agrícolas
          y a la calidad agroalimentaria.
        </p>
        <Motion
          :initial="{
            opacity: 0,
          }"
          :in-view="{ opacity: 1 }"
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
          class="mt-8"
          as="section"
        >
          <UButton to="/sobre-nosotros" color="green" size="lg" icon="i-heroicons-arrow-small-right"
            >Conoce más sobre nosotros</UButton
          >
        </Motion>
      </Motion>
    </section>

    <UDivider :ui="{ border: { base: 'dark:border-gray-200' } }" />

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -30,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Nuestros servicios</h2>
        <p class="text-xl mt-4 dark:text-black">
          Diagnósticos especializados para la sanidad y calidad agroalimentaria.
        </p>
      </Motion>

      <Motion
        as="section"
        :variants="container"
        initial="hidden"
        in-view="visible"
        :in-view-options="{ amount: 'some', once: true }"
        :transition="{
          type: 'spring',
          delayChildren: 0.3,
          staggerChildren: 0.2,
        }"
        class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8"
      >
        <Motion :variants="items" v-for="service in services">
          <ServiceCard
            :key="service.id"
            :title="service.title"
            :description="service.description"
            :image="service.image"
          />
        </Motion>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
        }"
        :in-view="{ opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
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
          x: -30,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">¿Por qué elegir CISEF?</h2>
      </Motion>

      <Motion
        as="section"
        :variants="container"
        initial="hidden"
        in-view="visible"
        :in-view-options="{ amount: 'some', once: true }"
        :transition="{
          type: 'spring',
          delayChildren: 0.3,
          staggerChildren: 0.2,
        }"
        class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8"
      >
        <Motion :variants="items" v-for="{ id, title, icon } in benefits">
          <BenefitCard :key="id" :title="title" :icon="icon" />
        </Motion>
      </Motion>
    </section>

    <section class="py-12">
      <Motion
        :initial="{
          opacity: 0,
          x: -30,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        as="section"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Sectores atendidos</h2>
        <p class="text-xl mt-4 dark:text-black">Soluciones específicas para cada área del sector agroalimentario</p>
      </Motion>

      <Motion
        :variants="container"
        initial="hidden"
        in-view="visible"
        :transition="{
          type: 'spring',
          delayChildren: 0.3,
          staggerChildren: 0.2,
          delay: 0.7,
        }"
        :in-view-options="{ amount: 'some', once: true }"
        class="flex justify-between items-center gap-8 py-12"
        as="section"
      >
        <Motion :variants="moveRight" class="w-1/2" as="section">
          <UCard
            :ui="{
              background: '',
              ring: '',
              shadow: '',
              base: 'w-full h-full min-h-full',
              body: { padding: '' },
            }"
          >
            <p class="md:text-3xl text-xl leading-snug italic dark:text-black">
              En <span class="font-bold text-primary">CISEF</span>, entendemos las necesidades únicas de cada sector
              dentro de la cadena agroalimentaria.
            </p>
          </UCard>
        </Motion>
        <Motion
          :variants="items"
          class="w-1/2 grid md:grid-cols-2 rounded-xl overflow-hidden min-h-full h-full"
          as="figure"
        >
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743209792/cisef/sectores-home1_clk6my.jpg"
            alt=""
            class="object-cover"
          />
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743209791/cisef/sectores-home2_rth6ai.jpg"
            alt=""
            class="object-cover"
          />
        </Motion>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          x: -30,
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
            y: 20,
          }"
          :in-view="{ y: 0, opacity: 1 }"
          :in-view-options="{ amount: 'all', once: true }"
          :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
          class="md:w-1/2 grid grid-cols-2 rounded-xl overflow-hidden shadow-pinterest h-full min-h-full"
          as="figure"
        >
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743209792/cisef/sectores-home3_qpuuft.jpg"
            alt=""
            class="object-cover"
          />

          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1743209791/cisef/sectores-home4_frpkkl.jpg"
            alt=""
            class="object-cover"
          />
        </Motion>
        <Motion
          :initial="{
            opacity: 0,
            x: -30,
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
                <span class="text-xl dark:text-black">{{ sector }}</span>
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
          x: -30,
        }"
        :in-view="{ x: 0, opacity: 1 }"
        :in-view-options="{ amount: 'all', once: true }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 } }"
        as="section"
      >
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Nuestras Certificaciones</h2>
        <p class="text-xl mt-4 dark:text-black">Reconocimientos que respaldan nuestra calidad y confiabilidad</p>
      </Motion>

      <Motion
        :initial="{
          opacity: 0,
          y: 20,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'some', once: true }"
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
              ring: 'dark:ring-gray-200',
              divide: 'dark:divide-gray-200',
            }"
          >
            <template #header>
              <h3 class="md:text-3xl text-xl font-bold dark:text-black">Certificados nacionales e internacionales</h3>
            </template>

            <section class="flex flex-col md:flex-row md:justify-between gap-12">
              <div class="">
                <h4 class="font-bold text-primary text-center">SADER</h4>
                <ul class="flex flex-col gap-8 pt-4">
                  <li class="flex items-center gap-2">
                    <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                    <section class="flex flex-col dark:text-black">
                      <span class="font-bold text-xl">Bacteriología:</span>
                      <span>LAB-260324-07-BACT-003</span>
                    </section>
                  </li>
                  <li class="flex items-center gap-2">
                    <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                    <section class="flex flex-col dark:text-black">
                      <span class="font-bold text-xl">Micología:</span>
                      <span>LAB-260324-07-MICO-003</span>
                    </section>
                  </li>
                  <li class="flex items-center gap-2">
                    <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                    <section class="flex flex-col dark:text-black">
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
                    <section class="flex flex-col dark:text-black">
                      <span class="font-bold text-xl">Sanidad agropecuaria:</span>
                      <span>SA-096-006/09</span>
                    </section>
                  </li>
                  <li class="flex items-center gap-2">
                    <Icon name="i-hugeicons-certificate-01" size="32" class="text-green-500" />
                    <section class="flex flex-col dark:text-black">
                      <span class="font-bold text-xl">Alimentos:</span>
                      <span>A-1512-136/22</span>
                    </section>
                  </li>
                </ul>
              </div>
            </section>
            <section class="flex flex-col md:items-center gap-2 pt-12 md:pt-8">
              <h4 class="text-center font-bold text-primary">INTERNACIONALES</h4>
              <span class="flex items-center gap-2 dark:text-black"
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
          :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
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
          x: -30,
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
          y: 20,
        }"
        :in-view="{ y: 0, opacity: 1 }"
        :in-view-options="{ amount: 'some', once: true }"
        :transition="{ duration: 0.5, y: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="flex flex-col md:flex-row justify-between mt-8 gap-8"
        as="section"
      >
        <UCard
          class="md:w-1/2"
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
        <UCard
          class="md:w-1/2 overflow-hidden min-h-full"
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
      <Motion
        :initial="{
          opacity: 0,
        }"
        :in-view="{ opacity: 1 }"
        :transition="{ duration: 1, x: { type: 'spring', stiffness: 260, damping: 20 }, delay: 0.3 }"
        class="mt-8 flex justify-center"
        as="section"
      >
        <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
      </Motion>
    </section>
  </UContainer>
</template>
