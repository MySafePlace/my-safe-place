<template>
  <footer class="footer">
    <section class="footer__logo">
      <img
        class="footer__logo__img"
          alt="logo"
          src="../components/assets/logo.png"
          />
      <span class="ml-3 text-2xl">Saviour Care</span>
    </section>
    <p class="text-l">
      © 2022 MySafePlace. Todos los derechos reservados.
    </p>
    <span class="inline-flex ">
      <a class="text-white">
        <svg
          fill="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-8 h-8"
          viewBox="0 0 24 24"
        >
          <path
            d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"
          ></path>
        </svg>
      </a>
      <a class="ml-3 text-white">
        <svg
          fill="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-8 h-8"
          viewBox="0 0 24 24"
        >
          <path
            d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"
          ></path>
        </svg>
      </a>
      <a class="ml-3 text-white">
        <svg
          fill="none"
          stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-8 h-8"
            viewBox="0 0 24 24"
          >
            <rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
            <path
              d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37zm1.5-4.87h.01"
            ></path>
          </svg>
        </a>
        <a class="ml-3 text-white">
          <svg
            fill="currentColor"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="0"
            class="w-8 h-8"
            viewBox="0 0 24 24"
          >
            <path
              stroke="none"
              d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"
            ></path>
            <circle cx="4" cy="4" r="2" stroke="none"></circle>
          </svg>
        </a>
      </span>
  </footer>
</template>

<script>
export default {
  name: 'PageFooter',
}
</script>

<style lang="scss">
.footer{
    width: 100%;
    height: var(--y-header);
    background: rgb(208,176,225);
    background: linear-gradient(90deg, rgba(208,176,225,1) 0%, rgba(170,208,255,1) 100%);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 var(--x-padding);
    color: white;
    @media (max-width: "768px") {
      flex-direction: column;
      justify-content: center;
      gap: 0.8rem;
      height: 15rem;
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
    a{
      transition: 0.4s;
      cursor: pointer;
      &:hover{
        color: #462e6a;
      }
    }
}
</style>
