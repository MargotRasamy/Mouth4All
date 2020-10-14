<template>
  <div class="hero">

    <div class="hero-section">
        <HeroCaption />
        <img src="https://via.placeholder.com/450" />

    </div>
    
  </div>
</template>

<script>

import HeroCaption from './HeroCaption.vue'

export default {
  name: 'Hero',
  components: {
    HeroCaption
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/variables/colors.scss";
@import "../../assets/variables/spaces.scss";
@import "../../assets/variables/medias.scss";
@import "../../assets/variables/misc.scss";
@import "../../assets/variables/reset.scss";

.hero {
  margin: 0;
  padding: 0 var(--gutterWidth);
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: var(--colorPrimaryVeryLight);
}

.hero-section {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin: auto;
    @include small{
      flex-direction: column;
      text-align: center;
    }
    @include medium{
      flex-direction: column;
      text-align: center;
    }
}

</style>
