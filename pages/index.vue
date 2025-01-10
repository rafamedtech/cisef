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
        <img
          src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/Valores_gti5x1.png"
          alt=""
          class="w-full"
        />
      </figure>
    </section>

    <UDivider />

    <section class="py-12 flex flex-col md:flex-row justify-between gap-8 items-center">
      <figure class="md:w-1/3 h-full rounded-xl overflow-hidden">
        <img src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/hero_vbzg9x.jpg" alt="" />
      </figure>
      <div class="md:w-1/2">
        <h2 class="md:text-5xl text-4xl font-semibold text-primary">Sobre CISEF</h2>
        <p class="text-xl mt-4">
          Desde 1997, somos un laboratorio certificado por SADER que contribuye al manejo sostenible de plagas agrícolas
          y a la calidad agroalimentaria.
        </p>
      </div>
    </section>

    <UDivider />

    <section class="py-12">
      <h2 class="md:text-5xl text-4xl font-semibold text-primary">Nuestros servicios</h2>
      <p class="text-xl mt-4">Diagnósticos especializados para la sanidad y calidad agroalimentaria.</p>
      <section class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8">
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
      </section>

      <section class="flex justify-center mt-8">
        <UButton to="/" color="green" size="lg" icon="i-heroicons-arrow-small-right"
          >Conoce más sobre nuestros servicios</UButton
        >
      </section>
    </section>

    <section class="py-12">
      <h2 class="md:text-5xl text-4xl font-semibold text-primary">¿Por qué elegir CISEF?</h2>

      <section class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8">
        <UCard>
          <section class="flex flex-col gap-8 py-12">
            <Icon name="hugeicons:certificate-01" size="64" class="text-green-500" />
            <span class="text-2xl">Reconocimientos nacionales e internacionales</span>
          </section>
        </UCard>

        <UCard>
          <section class="flex flex-col gap-8 py-12">
            <Icon name="hugeicons:dashboard-speed-01" size="64" class="text-green-500" />
            <span class="text-2xl">Resultados confiables y rápidos</span>
          </section>
        </UCard>

        <UCard>
          <section class="flex flex-col gap-8 py-12">
            <Icon name="hugeicons:user-check-01" size="64" class="text-green-500" />
            <span class="text-2xl">Personal calificado y tecnología de vanguardia</span>
          </section>
        </UCard>
        <UCard>
          <section class="flex flex-col gap-8 py-12">
            <Icon name="hugeicons:checkmark-square-03" size="64" class="text-green-500" />
            <span class="text-2xl">Transparencia e imparcialidad en los diagnósticos</span>
          </section>
        </UCard>
      </section>
    </section>

    <section class="py-12">
      <h2 class="md:text-5xl text-4xl font-semibold text-primary">Certificaciones y Reconocimientos</h2>

      <section class="grid grid-cols-1 md:grid-cols-4 gap-8 mt-8">
        <UCard>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/iso9001-2015_vzqz9v.jpg"
            alt=""
            class="w-full"
          />
        </UCard>
        <UCard>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/iso17025-2017_wnzv9v.jpg"
            alt=""
            class="w-full"
          />
        </UCard>
        <UCard>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/iso14001-2015_vzqz9v.jpg"
            alt=""
            class="w-full"
          />
        </UCard>
        <UCard>
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736539669/cisef/iso45001-2018_vzqz9v.jpg"
            alt=""
            class="w-full"
          />
        </UCard>
      </section>
    </section>

    <section class="py-12">
      <h2 class="md:text-5xl text-4xl font-semibold text-primary">Contáctanos</h2>
      <section class="flex flex-col md:flex-row justify-between mt-8 gap-8">
        <UCard class="md:w-1/2">
          <div class="flex flex-col gap-8">
            <section class="flex flex-col gap-2">
              <h3 class="text-2xl font-bold">Dirección</h3>
              <p class="font-light">Francisco de Urdiñola No. 360, Saltillo, Coahuila, México. C.P. 25000.</p>
            </section>
            <section class="flex flex-col gap-2">
              <h3 class="text-2xl font-bold">Teléfonos y correo</h3>
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
        <UCard class="md:w-1/2">
          <ClientOnly>
            <div style="width: 100%">
              <iframe
                width="100%"
                height="350"
                frameborder="0"
                scrolling="no"
                marginheight="0"
                marginwidth="0"
                src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=Francisco%20de%20Urdi%C3%B1ola%20No.%20360,%20Saltillo,%20Coahuila,%20M%C3%A9xico.%20C.P.%2025000.+(CISEF)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
              ></iframe>
            </div>
          </ClientOnly>
        </UCard>
      </section>
      <section class="mt-8 flex justify-center">
        <UButton to="/" color="green" size="lg" icon="i-heroicons-arrow-small-right">Agendar una cita</UButton>
      </section>
    </section>
  </UContainer>
</template>
