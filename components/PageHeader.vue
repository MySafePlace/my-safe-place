<template>
  <header class="header">
    <section class="header__logo">
        <img
          class="header__logo__img"
          alt="logo"
          src="../components/assets/logo.png"
          />
        <span class="text-3xl ml-4 font-semibold">MySafePlace</span>
    </section>
    <nav class="header__nav text-2xl">
      <a href="#inicio" class="header__nav__ancle">Inicio</a>
      <a href="#estadisticas" class="header__nav__ancle">Estadísticas</a>
      <a href="#comentarios" class="header__nav__ancle">Comentarios</a>
      <a href="#sobrenosotros" class="header__nav__ancle">Sobre Nosotros</a>
      <a href="#contactenos" class="header__nav__ancle">Contáctenos</a>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'PageHeader',
}
</script>

<style lang="scss">
  .header{
    width: 100%;
    height: var(--y-header);
    background: rgb(208,176,225);
    background: linear-gradient(90deg, rgba(208,176,225,1) 0%, rgba(170,208,255,1) 100%);
    position: fixed;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 var(--x-padding);
    @media (max-width: "768px") {
      flex-direction: column;
      width: 100%;
      padding: 1.6rem var(--x-padding);
    }
    @media (max-width: "540px") {
      position: absolute;
    }
    &__logo {
      width: auto;
      display: flex;
      align-items: center;
      color: white;
      &__img{
        background-color: #efefef;
        padding: 1rem;
        border-radius: 2.5rem;
      }
    }
    &__nav {
      width: 60%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 2rem;
      color: white;
      @media (max-width: "1024px") {
        gap: 1.6rem;
      }
      @media (max-width: "768px") {
        gap: 2rem;
        width: 100%;
      }
      @media (max-width: "540px") {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
      }
      &__ancle{
        transition: 0.4s;
        text-align: center;
        @media (max-width: "540px") {
          &:first-child{
            display: none;
          }
        }
        &:hover{
          font-size: 1.8rem;
          font-weight: bold;
        }
      }
    }
  }
</style>
