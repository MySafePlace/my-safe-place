<template>
  <section class="comments text-white">
    <h1 class="comments__title text-4xl">
          ¿Qué opinan nuestros usuarios sobre nosotros?
    </h1>  
    <div class="lg:w-1/3 flex flex-col sm:flex-row sm:items-center items-start mx-auto">
        
      </div>
      <div class="my-8 w-56 h-2 justify-self-center bg-white">
      </div>
  </section>
</template>

<script>
export default {
  name: 'CtaSection',
}
</script>

<style lang="scss">
  .comments{
    height: 20rem;
    background: rgb(208,176,225);
    background: linear-gradient(90deg, rgba(208,176,225,1) 0%, rgba(170,208,255,1) 100%);
    border-radius: 5rem;
    margin: 2rem var(--x-padding) 10rem;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-weight: bold;
    text-align: center;
  }
</style>