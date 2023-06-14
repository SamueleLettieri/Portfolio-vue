<template>
  <div id="app">
    <HeaderPortafolio />
    <main-portfolio />
    <footer-portafolio />
  </div>
</template>

<script>
import FooterPortafolio from './components/Footer/FooterPortafolio.vue';
import HeaderPortafolio from './components/Header/HeaderPortfolio.vue';
import MainPortfolio from './components/Main/MainPortfolio.vue';

export default {
  name: 'App',
  components: {
    HeaderPortafolio,
    MainPortfolio,
    FooterPortafolio
  }
}
</script>

<style lang="scss">

</style>
