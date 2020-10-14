<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue'
    
export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">

/* Import des variables */
@import "./assets/variables/colors.scss";
@import "./assets/variables/spaces.scss";
@import "./assets/variables/medias.scss";
@import "./assets/variables/misc.scss";
@import "./assets/variables/reset.scss";
@import 'node_modules/bootstrap/scss/bootstrap';



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 0;
  margin:0;
}

body{
  padding: 0;
  margin:0;
  min-height: 100vh;
  background-color: var(--colorPurpleVeryLight);
}

</style>
