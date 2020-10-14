<template>
  <div id="app">
    
    <Hero />
    <Mouth />
  
  </div>
</template>

<script>
import Hero from './components/hero/Hero.vue'
import Mouth from './components/demo/Mouth.vue'  

export default {
  name: 'App',
  components: {
    Hero,
    Mouth
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
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;

}

body{
  padding: 0;
  margin:0;
  //background: linear-gradient(#031b63ea, #ec225fb3);
  background-color: var(--colorPrimaryVeryLight);
}

</style>
