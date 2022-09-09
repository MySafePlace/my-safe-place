<template>
  <section id="inicio" class="hero">
    <div class="hero__content">
      <h1 class="hero__content__title text-6xl font-bold text-txt2">
        Estamos para ayudarte, no estás sola
      </h1>
      <p class="hero__content__text text-2xl">
        ¿Necesitas ayuda? Aquí estamos para apoyarte en lo que necesites.
      </p>
      <button class="hero__content__button text-white rounded-full text-xl" @click="openChat" >
          Empezar 
      </button>
    </div>
    <div class="hero__container">
      <img
        class="hero__container__img"
        alt="image1"
        src="../components/assets/image1.png"
        />
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
}
</script>

<style lang="scss">
.hero{
  padding: var(--y-header) calc(var(--x-padding)) 0;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  height: 48rem;
  gap: 3.6rem;
  @media (max-width: "768px") {
    grid-template-columns: 1fr;
    text-align: center;
  }
  &__content{
    display: flex;
    gap: 1.6rem;
    flex-direction: column;
    align-items: flex-start;
    @media (max-width: "768px") {
      align-items: center;
    }
    &__button{
      padding: 1rem 3rem;
      background-color: #9C89B8;
      transition: 1s;
      &:hover{
        background-color: #F0A6CA;
      }
    }
    &__text{
      color: #555;
    }
  }
  &__container{
    display: flex;
    justify-content: flex-end;
    @media (max-width: "768px") {
      display: none;
    }
    &__img{
      width: 90%;
    }
  }
}
</style>
