<template>
  <div class="main">
      <navigation class="topbar" msg="Please choose where you would like to go"></navigation>
      <hero class="hero-module"></hero>
      <services class="services-module"></services>
      <about class="about-module"></about>
      <faq class="faq-module"></faq>
  </div>
</template>

<script>
import navigation from './Navigation.vue';
import hero from './Hero.vue';
import services from './Services.vue';
import about from './About.vue';
import faq from './FAQ.vue';

export default {
  name: 'Main',
  components: {
    navigation, hero, services, about, faq
  }
}
</script>
<style lang="scss">
   @import '../scss/main.scss'
</style>