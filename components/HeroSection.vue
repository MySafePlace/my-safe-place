  <template>
  <section class="text-gray-400 body-font">
    <div
      class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center"
    >
      <div
        class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
      >
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-txt1">
          Estamos para ayudarte, no estás sola
        </h1>
        <p class="mb-8 leading-relaxed text-txt2">
          ¿Necesitas ayuda? Aquí estamos para apoyarte en lo que necesites.
        </p>
        <div class="flex justify-center">
          <button
            class="inline-flex text-white bg-btn1 border-5 py-2 px-6 focus:outline-blue rounded-full text-lg "
          >
            Empezar
            
          </button>
        </div>
      </div>
      <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
        <img
            alt="image1"
            src="../components/assets/image1.png"
            />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
}
</script>
