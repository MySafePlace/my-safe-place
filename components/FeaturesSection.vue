<template>
  <section class="features">
    <div id="estadisticas" class="features__data flex">
      <img
        class="features__data__picture"
        alt="image2"
        src="../components/assets/image2.png"
      />
      <div class="features__data__content">
        <h1 class="features__data__content__title text-txt2 text-6xl">
          Estadísticas de casos de violencia      
        </h1>
        <div class="features__data__content__line w-80 h-2">
        </div>
        <p class="features__data__content__text text-xl text-justify">
          Actualmente en el país se han registrado un total de {{this.statistics.total}} casos que fueron atendidos en 
          “My Safe Place”, de los cuales, el
          {{((this.statistics.lima / this.statistics.total)*100).toFixed(2)}}% pertenece a Lima Metropolitana, 
          {{((this.statistics.arequipa / this.statistics.total)*100).toFixed(2)}}% Arequipa y 
          {{((this.statistics.others / this.statistics.total)*100).toFixed(2)}}% pertenecientes al resto de provincias del país. 
          Asimismo, se encontró evidencia de que el 70% de las mujeres que emplearon el chatbot, 
          no eran conscientes del gran riesgo en el cuál se encontraban.
        </p>
      </div>
    </div>
    <div id="comentarios" class="features__comments">
      <div class="features__comments__content">
        <h1 class="features__comments__content__title text-txt1 text-6xl">
          Comentarios
        </h1>
        <div class="features__comments__content__line w-60 h-2"></div>
        <div class="text-xl text-justify">
          Si deseas dejarnos alguna sugerencia y/o comentario acerca de tu experiencia en nuestro sitio web y con el empleo de nuestro chatbot, por favor da clic al siguiente botón
        </div>
        <button class="features__comments__content__button text-txtbtn1 border border-txtbtn1 rounded-full text-lg" @click="toggleForm">
            Deja tu comentario
        </button>
      </div>
      <img
          class="features__comments__picture"
          alt="image3"
          src="../components/assets/image3.png"
      />
    </div>
    <div v-if="formActive" class="features__form">
      <label class="features__form__text text-3xl" for="name">Nombre:</label>
      <input class="features__form__input" type="text">
      <label class="features__form__text text-3xl" for="comment">Comentario:</label>
      <textarea class="features__form__opinion" name="comment" id="comment" cols="30" rows="10"></textarea>
      <div class="features__form__buttons">
        <button class="features__form__buttons__button" @click="toggleForm">Cancelar</button>
        <button class="features__form__buttons__button" @click="sumbitOpinion">Enviar</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeaturesSection',
  methods: {
    toggleForm(){
      this.formActive = !this.formActive;
    },
    sumbitOpinion(){
      alert("Se envió con éxito");
      this.formActive = !this.formActive;
    },
  },
  data(){
    return {
      formActive: false,
      statistics: {
        lima: 8,
        arequipa: 4,
        others: 12,
        total: 24,
      },
    }
  }
}
</script>

<style lang="scss">
.features{
  height: auto;
  padding: 0 calc(var(--x-padding));
  &__data{
    height: 60rem;
    display: grid;
    align-items: center;
    gap: 2rem;
    grid-template-columns: repeat(2, 1fr);
    @media (max-width: "768px") {
      height: auto;
      grid-template-columns: 1fr;
      grid-template-rows: 40rem 1fr;
    }
    &__picture{
      height: 60rem;
      @media (max-width: "768px") {
        justify-self: center;  
        height: 40rem;
      }
    }
    &__content{
      display: flex;
      flex-direction: column;
      gap: 2rem;
      &__title{
        font-weight: bold;
      }
      &__line{
        background-color: rgba(255,180,209, 1);
      }
      &__text{
        color: #555;
      }
    }
  }
  &__comments{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    height: 40rem;
    gap: 2rem;
    @media (max-width: "768px") {
      padding: 5rem 0;
      height: 55rem;
      grid-template-columns: 1fr;
      grid-template-rows: 30rem 1fr;  
      grid-template-areas: "Img" "Text";
    }
    &__content{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 1.6rem;
      &__title{
        font-weight: bold;
      }
      &__line{
        background-color: rgba(205,180,219, 1);
      }
      &__text{
        color: #555;
      }
      &__button{
        transition: 1s;
        padding: 0.8rem 2.4rem;
        &:hover{
          color: white;
          background-color: #9c89B8;
        }
      }
    }
    &__picture{
        @media (max-width: "768px") {
          justify-self: center;
          height: 30rem;
          grid-area: Img;
        }
      }
  }
  &__form{
    width: 50vw;
    height: 70vh;
    top: 0;
    margin-top: 20vh;
    margin-left: 15vw;
    position: fixed;
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
    background: rgb(208,176,225);
    background: linear-gradient(90deg, rgba(208,176,225,1) 0%, rgba(170,208,255,1) 100%);
    border-radius: 7.5rem;
    padding: 5vh 7.5vw;
    @media (max-width: "768px") {
      width: 80vw;
      margin-top: 25vh;
      margin-left: 0;
    }
    @media (max-width: "540px") {
      padding: 4vh 6vw;
      border-radius: 5rem;
      width: 80vw;
      margin-top: 30vh;
      margin-left: 0;
      height: 60vh;
    }
    @media (max-width: "540px") {
      padding: 2vh 6vw;
      border-radius: 2.5rem;
    }
    &__input{
      padding: 0.6rem 1rem;
      border-radius: 1rem;
      font-size: 1.6rem;
      
    }
    &__text{
      color: white;
      font-weight: bold;
      @media (max-width: "540px") {
        font-size: 1.6rem;
      }
    }
    &__opinion{
      font-size: 1.2rem;
      padding: 0.6rem 1rem;
      border-radius: 2.4rem;
    }
    &__buttons{
      display: flex;
      justify-content: space-between;
      &__button{
        background-color: white;
        color: black;
        padding: 0.6rem 1.2rem;
        font-size: 1.6rem;
        border-radius: 1rem;
        transition: 0.6s;
        &:hover{
          transition: 0.6s;
          background-color: transparent;
          color: white;
          font-weight: bold;
        }
      }
    }
  }
}

</style>
