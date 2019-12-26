<template>
  <div id="app">
    <Main msg="Welcome to Businet"/>
  </div>
</template>

<script>
import Main from './components/Main.vue'

export default {
  name: 'app',
  components: {
    Main
  }
}
</script>

<style>
#app {
  /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000;
  /*margin-top: 60px;*/
}
</style>
<style lang="scss">
   body {
    // background: blue;
    
   }
</style>