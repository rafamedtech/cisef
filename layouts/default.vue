<script setup lang="ts"></script>

<template>
  <div class="p-4 bg-gradient-to-br from-blue-50 to-green-50 min-h-screen z-0">
    <header class="flex justify-between items-center h-24 z-20">
      <section class="h-full">
        <NuxtLink to="/">
          <img src="@/assets/images/logo.jpeg" alt="" class="w-full h-full" />
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
          <UButton to="/" color="green">Agenda una cita</UButton>
          <UButton to="/" color="green" icon="i-heroicons-bars-3-bottom-right" variant="outline" class="md:hidden" />
        </section>
      </nav>
    </header>
    <main class="relative">
      <slot />
    </main>
  </div>
</template>
