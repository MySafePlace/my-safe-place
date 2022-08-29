<template>
  <section class="text-gray-600 body-font">
    <div id="estadisticas" class="container px-5 py-24 mx-auto flex flex-wrap">
      <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
        <img
            alt="image2"
            src="../components/assets/image2.png"
            width="408"
            height="624"
            />
      </div>
      <div
        class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
      >
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-txt1">
          Estadísticas de casos de violencia      
      <div 
        class="my-8 w-56 h-2 items-center justify-center bg-txt1"
        >
      </div>
        </h1>
        <p class="mb-8 leading-relaxed text-txt3">
          Actualmente en el país se han registrado un total de ## casos que fueron atendidos en “My Safe Place”, de los cuales, el 50% pertenece a Lima Metropolitana, 10% Arequipa y 30% pertenecientes al resto de provincias del país. Asimismo, se encontró evidencia de que el 70% de las mujeres que emplearon el chatbot, no eran conscientes del gran riesgo en el cuál se encontraban.
        </p>
      </div>
    </div>

    <div id="comentarios" class="container px-5 py-24 mx-auto flex flex-wrap">
      <div
        class="lg:w-1/2 sm:w-1/3 w-full rounded-lg overflow-hidden mt-6 sm:mt-0"
      >
        <img
          alt="image3"
          src="../components/assets/image3.png"
        />
      </div>
      <div
        class="flex flex-wrap -mx-4 mt-auto mb-auto lg:w-1/2 sm:w-2/3 content-start sm:pr-10"
      >
        <div class="w-full sm:p-4 px-4 mb-6">
          <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-txt2">
            Comentarios
          </h1>
          <div 
        class="my-8 w-56 h-2 items-center justify-center bg-txt2"
        >
      </div>
      <div class="leading-relaxed text-txt3">
            Deseas dejarnos alguna sugerencia y/o comentario acerca de tu experiencia en nuestro sitio web y con el empleo de nuestro chatbot, por favor da clic al siguiente botón
          </div>
        </div>
        <button
            class="ml-4 inline-flex text-txtbtn1 py-2 px-6 border border-txtbtn1 focus:outline-none rounded-full text-lg"
          >
            Learn More
          </button>
      </div>
      
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeaturesSection',
}
</script>
