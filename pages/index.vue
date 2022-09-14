<template>
  <div>
    <HeroSection />
    <FeaturesSection />
    <StatisticsSection />
    <CtaSection />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'default',
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Mulish:wght@300;500;700&display=swap');

  html{
    font-size: 62.5%;
    scroll-behavior: smooth;
    font-family: 'Mulish', sans-serif;
    --x-padding: 15rem;
    --y-header: 8rem;
    scroll-padding-top: var(--y-header);
    @media (max-width: "1024px") {
    --x-padding: 10rem;
    }
    @media (max-width: "768px") {
    --x-padding: 7.5rem;
    --y-header: 12.5rem;
    }
    @media (max-width: "540px") {
    --x-padding: 5rem;
    --y-header: 16rem;
    }
    @media (max-width: "425px") {
    --x-padding: 3.5rem;
    }
  }
</style>
