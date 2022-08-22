<template>
  <header class="text-gray-500 body-font">
    <div
      class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
    >
    <a
        class="flex order-first lg:order-none title-font font-medium items-center text-secondary lg:items-center lg:justify-center mb-4 md:mb-0"
      >
        <div 
        class="w-12 h-12 inline-flex items-center justify-center rounded-full bg-logo"
        >
        <img
            alt="logo"
            src="../components/assets/logo.png"
            width="34"
            height="34"
            />
        </div>
        <span class="ml-3 text-xl font-semibold text-title">MySafePlace</span>
      </a>
      <nav class="flex lg:w-5/5 flex-wrap items-center text-base md:ml-auto">
        <nuxt-link to="/" class="mr-10 text-txtnav">Inicio</nuxt-link>
        <nuxt-link to="/chat" class="mr-10 text-txtnav">Estadísticas</nuxt-link>
        <a class="mr-10 text-txtnav">Comentarios</a>
        <nuxt-link to="/team" class="mr-10 text-txtnav"
          >Sobre Nosotros</nuxt-link
        >
        <a class="mr-10 text-txtnav">Contáctenos</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
}
</script>

