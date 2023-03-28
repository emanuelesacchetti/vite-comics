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
  <TheHeader></TheHeader>
  <main>
    <TheJumbotron></TheJumbotron>
    <ProductList></ProductList>
  </main>
  
  <TheFooter></TheFooter>
  <TheBlackBanner></TheBlackBanner>
</template>

<style lang="scss">
  @use './styles/general.scss';

 
  main {
    background-color: black;
  }
</style>
