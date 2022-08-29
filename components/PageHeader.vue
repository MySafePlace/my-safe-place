<template>
  <header class="sticky top-0 bg-txt2 text-gray-500 body-font">
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
        <a href="#inicio" class="mr-10 text-txtnav">Inicio</a>
        <a href="#estadisticas" class="mr-10 text-txtnav">Estadísticas</a>
        <a href="#comentarios" class="mr-10 text-txtnav">Comentarios</a>
        <a href="#sobrenosotros" class="mr-10 text-txtnav">Sobre Nosotros</a>
        <a href="#contactenos" class="mr-10 text-txtnav">Contáctenos</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
}
</script>

