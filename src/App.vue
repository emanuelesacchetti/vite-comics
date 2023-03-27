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
  <TheBlueBanner></TheBlueBanner>
  <TheFooter></TheFooter>
  <TheBlackBanner></TheBlackBanner>
</template>

<style lang="scss" scoped>
  @use "./styles/general.scss";
  
</style>
