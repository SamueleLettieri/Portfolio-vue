<template>
  <main class="mt-5">
    <welcome-main />
    <about-me-main />
    <skills-main />
  </main>
</template>

<script>
import AboutMeMain from './AboutMeMain.vue';
import SkillsMain from './SkillsMain.vue';
import WelcomeMain from './WelcomeMain.vue';

export default {
  components: {WelcomeMain, AboutMeMain, SkillsMain},

}
</script>

<style>

</style>