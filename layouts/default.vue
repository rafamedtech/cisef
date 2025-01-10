<script setup lang="ts"></script>

<template>
  <div class="p-4 bg-gradient-to-br from-blue-100 to-green-100 min-h-screen z-0">
    <header class="flex justify-between items-center h-24 z-20">
      <section class="h-full">
        <NuxtLink to="/">
          <img
            src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736543044/cisef/logo-removebg-preview_mn6twt.png"
            alt=""
            class="w-full h-full"
          />
        </NuxtLink>
      </section>
      <nav class="flex md:space-x-4 items-center">
        <ul class="space-x-12 hidden md:flex">
          <li>
            <NuxtLink to="/">Inicio</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/">Servicios</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/">Certificaciones</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/">Sectores atendidos</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/">Contacto</NuxtLink>
          </li>
        </ul>
        <section class="flex items-center space-x-2">
          <UButton to="/" color="green" icon="i-heroicons-calendar-days" size="lg">Agendar una cita</UButton>
          <UButton to="/" color="green" icon="i-heroicons-bars-3-bottom-right" variant="outline" class="md:hidden" />
        </section>
      </nav>
    </header>
    <main class="relative">
      <slot />
    </main>

    <UDivider />
    <UContainer class="py-8">
      <footer class="flex justify-between items-center max-h-24 h-24 z-20">
        <section class="h-full">
          <NuxtLink to="/">
            <img
              src="https://res.cloudinary.com/rafamed-dev/image/upload/v1736543044/cisef/logo-removebg-preview_mn6twt.png"
              alt=""
              class="w-full h-full"
            />
          </NuxtLink>
        </section>
        <nav>
          <ul class="flex gap-4">
            <li>
              <NuxtLink to="/">Servicios</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/">Certificaciones</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/">Sectores atendidos</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/">Contacto</NuxtLink>
            </li>
          </ul>
        </nav>
        <section class="flex items-center space-x-2">
          <UButton to="/" icon="i-hugeicons-facebook-01" size="xl" variant="ghost" />
          <UButton to="/" icon="i-hugeicons-instagram" size="xl" variant="ghost" />
          <UButton to="/" icon="i-hugeicons-linkedin-01" size="xl" variant="ghost" />
        </section>
      </footer>
    </UContainer>
  </div>
</template>
