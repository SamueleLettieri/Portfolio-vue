<template>
  <div id="app">
    <HeaderPortafolio />
    <main-portfolio />
  </div>
</template>

<script>
import HeaderPortafolio from './components/Header/HeaderPortfolio.vue';
import MainPortfolio from './components/Main/MainPortfolio.vue';

export default {
  name: 'App',
  components: {
    HeaderPortafolio,
    MainPortfolio
  }
}
</script>

<style lang="scss">

</style>
