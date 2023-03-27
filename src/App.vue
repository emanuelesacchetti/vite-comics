<script>
  import TheHeader from './components/TheHeader.vue';
  import TheFooter from './components/TheFooter.vue';
  import TheBlackBanner from './components/TheBlackBanner.vue';
  import TheBlueBanner from './components/TheBlueBanner.vue';

  export default {
    components: {
      TheHeader,
      TheFooter,
      TheBlueBanner,
      TheBlackBanner
    }
  }
</script>

<template>
  <TheHeader></TheHeader>
  <main></main>
  <TheBlueBanner></TheBlueBanner>
  <TheFooter></TheFooter>
  <TheBlackBanner></TheBlackBanner>
</template>

<style lang="scss">
  @use './styles/general.scss';

 
  main {
    height: calc(100vh - (250px + 70px + 70px));
    width: 100%;
    background-color: black;
  }
</style>
