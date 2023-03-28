<script>
  import TheHeader from './components/TheHeader.vue';
  import TheFooter from './components/TheFooter.vue';
  import TheBlackBanner from './components/TheBlackBanner.vue';
  import TheBlueBanner from './components/TheBlueBanner.vue';
  import TheJumbotron from './components/TheJumbotron.vue';
  import ProductList from './components/ProductList.vue';

  export default {
    components: {
      TheHeader,
      TheFooter,
      TheBlueBanner,
      TheBlackBanner,
      TheJumbotron,
      ProductList
    }
  } 
  
</script>

<template>
  <TheHeader />
  <main>
    <TheJumbotron />
    <ProductList />
  </main>
  
  <TheFooter />
  <TheBlackBanner />
</template>

<style lang="scss">
  @use './styles/general.scss';


  main {
    background-color: #1c1c1c;
  }
</style>
