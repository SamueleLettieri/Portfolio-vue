<template>
  <div id="app">
    <HeaderPortafolio />
    <main-portfolio class="pb-5" />
    <footer-portafolio class="mt-5" />
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
