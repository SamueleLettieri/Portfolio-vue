<template>
  <main class="mt-5">
    <welcome-main />
    <about-me-main />
    <skills-main />
    <works-main />
  </main>
</template>

<script>
import AboutMeMain from './AboutMeMain.vue';
import SkillsMain from './SkillsMain.vue';
import WelcomeMain from './WelcomeMain.vue';
import WorksMain from './WorksMain.vue';

export default {
  components: {WelcomeMain, AboutMeMain, SkillsMain, WorksMain},

}
</script>

<style>

</style>