<script setup lang="ts">
const isOpen = ref(false);

const links = [
  { label: 'Inicio', to: '/' },
  { label: 'Sobre nosotros', to: '/sobre-nosotros' },
  { label: 'Servicios', to: '/servicios' },
  { label: 'Certificaciones', to: '/certificaciones' },
  { label: 'Contacto', to: '/contacto' },
];

function handleClick(link: any) {
  isOpen.value = !isOpen.value;
  return navigateTo(link.to);
}
</script>

<template>
  <div class="p-4 bg-gradient-to-br from-blue-100 to-green-100 min-h-screen z-0">
    <header class="flex justify-between items-center h-24 z-20">
      <section class="w-20 h-full">
        <NuxtLink to="/">
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736543044/cisef/logo-removebg-preview_mn6twt.png"
            alt=""
            class="w-full h-full"
          />
        </NuxtLink>
      </section>
      <nav class="flex md:space-x-12 items-center">
        <ul class="space-x-12 hidden md:flex">
          <li v-for="link in links" :key="link.to">
            <NuxtLink :to="link.to" :class="link.to === $route.path ? 'text-green-500 underline' : ''">{{
              link.label
            }}</NuxtLink>
          </li>
        </ul>
        <section class="flex items-center space-x-2">
          <UButton to="/agendar-cita" color="green" icon="i-heroicons-calendar-days" size="lg"
            >Agendar una cita</UButton
          >
          <UButton
            color="green"
            icon="i-heroicons-bars-3-bottom-right"
            variant="outline"
            class="md:hidden"
            @click="isOpen = true"
            size="lg"
          />
        </section>
      </nav>
    </header>

    <UModal v-model="isOpen" fullscreen>
      <UCard
        :ui="{
          base: 'h-screen flex flex-col',
          background: 'bg-gradient-to-br from-blue-100 to-green-100',
          rounded: '',
          divide: 'divide-y divide-gray-100 dark:divide-gray-800',
          body: {
            base: 'grow',
          },
        }"
      >
        <template #header>
          <div class="flex items-center justify-between">
            <h3 class="text-xl font-semibold leading-6 text-primary">Menú de navegación</h3>
            <UButton
              color="gray"
              variant="ghost"
              icon="i-heroicons-x-mark-20-solid"
              class="-my-1"
              @click="isOpen = false"
            />
          </div>
        </template>

        <nav class="h-full flex justify-center items-center">
          <ul class="flex flex-col gap-4 items-center justify-center">
            <li v-for="link in links" :key="link.to">
              <UButton
                @click="handleClick(link)"
                variant="link"
                size="xl"
                color="white"
                :class="link.to === $route.path ? 'text-green-500 underline' : ''"
                ><span class="text-2xl">{{ link.label }}</span></UButton
              >
            </li>
          </ul>
        </nav>
      </UCard>
    </UModal>
    <main class="relative">
      <slot />
    </main>

    <UDivider />
    <UContainer class="md:py-8 pt-8">
      <footer class="flex flex-col gap-4 md:flex-row justify-between items-center md:max-h-24 md:h-24 z-20">
        <section class="w-20 h-24 md:h-full">
          <NuxtLink to="/">
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736543044/cisef/logo-removebg-preview_mn6twt.png"
              alt=""
              class="w-full h-full"
            />
          </NuxtLink>
        </section>
        <nav>
          <ul class="flex flex-col md:flex-row md:gap-12">
            <li v-for="link in links" :key="link.to">
              <NuxtLink :to="link.to" :class="link.to === $route.path ? 'text-green-500 underline' : ''">{{
                link.label
              }}</NuxtLink>
            </li>
          </ul>
        </nav>
        <section class="flex items-center space-x-2">
          <UButton
            to="http://facebook.com/soycisef"
            target="_blank"
            icon="i-hugeicons-facebook-01"
            size="xl"
            variant="ghost"
          />
          <UButton
            to="https://www.instagram.com/cisef.lab?igsh=MTExdGhlZW5tZnRpMg=="
            target="_blank"
            icon="i-hugeicons-instagram"
            size="xl"
            variant="ghost"
          />
          <UButton
            to="http://linkedin.com/company/cisef-labs"
            target="_blank"
            icon="i-hugeicons-linkedin-01"
            size="xl"
            variant="ghost"
          />
        </section>
      </footer>
    </UContainer>
  </div>
</template>
