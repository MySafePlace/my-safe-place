<template>
  <section class="features">
    <div id="sobrenosotros" class="features__information">
      <img
        class="features__information__picture"
        alt="image4"
        src="../components/assets/image4.png"
      />
      <div class="features__information__content">
        <h1 class="features__information__content__title text-6xl">
          Sobre Nosotros
        </h1>
        <div class="features__information__content__line w-60 h-2"></div>
        <div class="text-xl text-justify">
          Somos “My Safe Place”, la cual tiene como propósito brindar apoyo psicológico a las mujeres que han sido violentadas...
        </div>
      </div>
    </div>
    <div id="contactenos" class="features__contact">
      <div class="features__contact__content">
        <h1 class="features__contact__content__title text-txt1 text-6xl">
          Contáctenos
        </h1>
        <div class="features__contact__content__line w-60 h-2"></div>
        <div class="text-xl text-justify">
          Para mayor información, sírvase contactarnos dándole clic al botón de a continuación
        </div>
      </div>
      <img
        class="features__contact__picture"
        alt="image5"
        src="../components/assets/image5.png"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: 'StatisticsSection',
}
</script>

<style lang="scss">
  .features{
    height: auto;
    padding: 0 calc(var(--x-padding));
    &__information{
      height: 40rem;
      display: grid;
      align-items: center;
      gap: 2rem;
      grid-template-columns: repeat(2, 1fr);
      @media (max-width: "768px") {
        height: auto;
        grid-template-columns: 1fr;
        grid-template-rows: 30rem 1fr;
      }
      &__picture{
        @media (max-width: "768px") {
          justify-self: center;
          height: 30rem;
        }
      }
      &__content{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 2rem;
        &__title{
          font-weight: bold;
          color: rgb(70,46,106);
        }
        &__line{
          background-color: rgba(70,46,106, 1);
        }
        &__text{
          color: #555;
        }
      }
    }
    &__contact{
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      align-items: center;
      height: 40rem;
      gap: 2rem;
      @media (max-width: "768px") {
        padding: 5rem 0;
        height: auto;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 20rem;
      }
      &__picture{
        @media (max-width: "768px") {
          justify-self: center;
          height: 20rem;
        }
      }
      &__content{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 1.6rem;
        &__title{
          font-weight: bold;
          color: rgb(131,217,236);
        }
        &__line{
          background-color: rgba(131,217,236, 1);
        }
        &__text{
          color: #555;
        }
      }
    }
  }

  </style>