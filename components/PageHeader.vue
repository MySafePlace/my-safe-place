<template>
  <header class="text-gray-500 body-font">
    <div
      class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
    >
      <nav class="flex lg:w-2/5 flex-wrap items-center text-base md:ml-auto">
        <nuxt-link to="/" class="mr-5 hover:text-gray-900">Inicio</nuxt-link>
        <nuxt-link to="/chat" class="mr-5 hover:text-gray-900">Chat</nuxt-link>
        <nuxt-link to="/team" class="mr-5 hover:text-gray-900"
          >Equipo</nuxt-link
        >
        <a class="hover:text-gray-900">Contacto</a>
      </nav>
      <a
        class="flex order-first lg:order-none lg:w-1/5 title-font font-medium items-center text-secondary lg:items-center lg:justify-center mb-4 md:mb-0"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-10 h-10 text-white p-2 bg-tangerine rounded-full"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
          />
        </svg>
        <span class="ml-3 text-xl font-semibold">MySafePlace</span>
      </a>
      <div class="lg:w-2/5 inline-flex lg:justify-end ml-5 lg:ml-0">
        <nuxt-link
          to="/chat"
          class="inline-flex items-center bg-secondary border-0 py-1 px-3 focus:outline-none hover:bg-indigo-400 rounded text-white mt-4 md:mt-0"
        >
          Ingresar al Chat
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-4 h-4 ml-1"
            viewBox="0 0 24 24"
          >
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </nuxt-link>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
}
</script>
