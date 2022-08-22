<template>
  <section class="text-gray-600 body-font">
    <div class="container px-5 py-24 mx-auto flex flex-wrap">
      <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
        <img
            alt="image2"
            src="../components/assets/image2.png"
            />
      </div>
      <div
        class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
      >
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-txt1">
          Estadísticas de casos de violencia
          <!--
		  <br class="hidden lg:inline-block" />
		  -->
      
      <div 
        class="w-56 h-2 items-center justify-center bg-txt1"
        >
      </div>
        </h1>
        <p class="mb-8 leading-relaxed text-txt3">
          Actualmente en el país se han registrado un total de ## casos que fueron atendidos en “My Safe Place”, de los cuales, el 50% pertenece a Lima Metropolitana, 10% Arequipa y 30% pertenecientes al resto de provincias del país. Asimismo, se encontró evidencia de que el 70% de las mujeres que emplearon el chatbot, no eran conscientes del gran riesgo en el cuál se encontraban.
        </p>
        <div class="flex justify-center">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeaturesSection',
}
</script>
