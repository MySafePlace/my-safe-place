<template>
  <section class="comments text-white">
    <h1 class="comments__title text-4xl">
          ¿Qué opinan nuestros usuarios sobre nosotros?
    </h1>
    <div class="my-8 w-56 h-2 justify-self-center bg-white">
    </div>
    <div class="comments__container">
      <article class="comments__container__comment" v-for="comment in comments" :key="comment.fullname">
        <p class="comments__container__comment__fullname">{{ comment.fullname }}</p>
        <p class="comments__container__comment__content">{{ comment.comment }}</p>
        <br/>
      </article>
    </div>
  </section>
</template>

<script>
import axios from "axios";

export default {
  name: 'CtaSection',
  data(){
    return {
      comments: [],
    }
  },
  mounted() {
    axios.get("https://comentarios-tdp.herokuapp.com/api/v1/comentario")
        .then((data) =>{
          this.comments.push(data.data[data.data.length - 1]);
          this.comments.push(data.data[data.data.length - 2]);
        })
        .catch((error) => {
          console.log(error.response);
       })
      this.formActive = !this.formActive;
  }
}
</script>

<style lang="scss">
  .comments{
    scroll-snap-align: start;
    height: auto;
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
    &__container{
      &__comment{
        &__fullname{
          font-size: 2rem;
        }
        &__content{
          font-size: 1.6rem;
          font-weight: 400;
        }
      }
    }
  }
</style>
