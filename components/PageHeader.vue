<template>
  <header class="header">
    <section class="header__logo">
        <img
          class="header__logo__img"
          alt="logo"
          src="../components/assets/logo.png"
          />
        <span class="text-3xl ml-4 font-semibold">MySafePlace</span>
        <div @click="toggleMenu" class="Burger-Container">
          <div class="menu-btn">
            <div class="menu-btn__burger"></div>
          </div>
        </div>
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
  data(){
    return {
      menuOpen: false,
    }
  },
  methods: {
    toggleMenu(){
      const menuBtn = document.querySelector('.menu-btn');
      const nav = document.querySelector('.header__nav');
      const headerAll = document.querySelector('.header');
      if(!this.menuOpen) {
        menuBtn.classList.add('open');
        this.menuOpen = true;
        nav.classList.add('active');
        headerAll.classList.add('active');
      } else {
        menuBtn.classList.remove('open');
        this.menuOpen = false;
        nav.classList.remove('active');
        headerAll.classList.remove('active');
      }
    }
  }
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
      height: 8rem;
      &.active{
        height: var(--y-header);
      }
    }
    @media (max-width: "540px") {
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
        display: none;
        gap: 2rem;
        width: 100%;
        &.active{
          animation: fadeIn 1.5s;
          display: flex;
        }
        @keyframes fadeIn {
          0% { opacity: 0; }
          100% { opacity: 1; }
        }
      }
      @media (max-width: "540px") {
        display: none;
        grid-template-columns: repeat(2, 1fr);
        &.active{
          animation: fadeIn 0.5s;
          display: grid;
        }
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
.Burger-Container{
  position: fixed;
  right: 10px;
}
.menu-btn {
  display: none;
  @media (max-width: "768px") {
    display: flex;
  }
  justify-content: center;
  align-items: center;
  width: 80px;
  height: 40px;
  cursor: pointer;
  transition: all .5s ease-in-out;
  @media (max-width: "540px") {
    right: 0;
  }
  /* border: 3px solid #fff; */
  &__burger {
    width: 50px;
    height: 4px;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(255,101,47,.2);
    transition: all .5s ease-in-out;
    &::before,
    &::after {
      content: '';
      position: absolute;
      width: 50px;
      height: 4px;
      background: #fff;
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(255,101,47,.2);
      transition: all .5s ease-in-out;
    }
    &::before {
      transform: translateY(-16px);
    }
    &::after {
      transform: translateY(16px);
    }
  }
}
/* ANIMATION */
.menu-btn.open .menu-btn__burger {
  transform: translateX(-50px);
  background: transparent;
  box-shadow: none;
}
.menu-btn.open .menu-btn__burger::before {
  transform: rotate(45deg) translate(35px, -35px);
}
.menu-btn.open .menu-btn__burger::after {
  transform: rotate(-45deg) translate(35px, 35px);
}
</style>
