<template>
  <div id="app">
    
    <Hero data-background="section1"  />
    <Demos data-background="section2" />
    <!-- <Mouth data-background="section2" id="demo" /> -->
    <Video data-background="section3" id="demo" />
    <Gamification2 data-background="section4" />
    <Gamification data-background="section4" />
    <Crowdfunding data-background="section5" id="crowd" />
    
  
  </div>
</template>

<script>
import Hero from './components/hero/Hero'
import Demos from './components/demo/Demos'
import Video from './components/video/Video'
import Crowdfunding from './components/crowdfund/Crowdfunding'
import Gamification from './components/demo/Gamification'
import Gamification2 from './components/demo/Gamification2'

export default {
  name: 'App',
  components: {
    Hero,
    Demos,
    Video,
    Crowdfunding,
    Gamification,
    Gamification2,
  }, 
  mounted() {
      const colors = ['color-section1', 'color-section2', 'color-section3', 'color-section4', 'color-section5', 'color-section5']

      const sections = document.querySelectorAll('div[data-background]')

      window.addEventListener('scroll', function () {

        const scrollFromTop = window.scrollY



        for (let i = 0; i < sections.length; i++) {

          if (scrollFromTop <= (sections[i].offsetTop + 500) ) {
            document.body.className = colors[i] 
            break
          } 

        }

      })
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

@font-face {
  font-family: 'DMSans' ;
  src: url("./assets/fonts/DM_Sans/DMSans-Regular.ttf");
}

#app {
  font-family: DMSans;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;

}

html::-webkit-scrollbar {
  width: 10px;
  background-color: var(--colorPrimaryVeryLight); 
}
html::-webkit-scrollbar-thumb {
    background: var(--colorPrimary); 
}

body{
  padding: 0;
  margin:0;
  //background: linear-gradient(#031b63ea, #ec225fb3);

  transition: all 0.5s ease;
}

.color-section1 {
   background-color: var(--colorWhite);
  // background-image: url('./assets/images/bg.jpg');
  // background-size: contain;
}
.color-section2 {
  background-color: var(--colorSecondaryLight);
}
.color-section3 {
  background-color:var(--colorSecondaryLight);
}
.color-section4 {
  background-color:var(--colorPrimaryVeryLight);
}
.color-section5 {
  background-color:var(--colorPrimaryLight);
}

</style>
