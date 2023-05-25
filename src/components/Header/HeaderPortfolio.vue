<template>
  <header>
    <navbar-header />
    <carosel-header />
  </header>
</template>

<script>
import CaroselHeader from './CaroselHeader.vue'
import NavbarHeader from './NavbarHeader.vue'
export default {
  components: 
  { 
    NavbarHeader,
    CaroselHeader
  },

}
</script>

<style lang="scss" scoped>

</style>