<template>
  <div class="hero">
    <Header />
    <div class="hero-section">
        <HeroCaption />
        <div class="hero-content">
          <div class="hero-image">
            <img class="image" src="../../assets/images/children.svg" />
          </div>
        </div>
        
        

    </div>
    
  </div>
</template>

<script>

import HeroCaption from './HeroCaption.vue'
import Header from './Header.vue'
export default {
  name: 'Hero',
  components: {
    HeroCaption,
    Header
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
  background: linear-gradient(#704edf2b, #608edd90);
  
}
.hero-content {
  width: 50%;
  .hero-image {
    width: 70%;
    margin: auto;
  }
  .image {
    object-fit: cover;
    width: 100%;
  }
}



.hero-section {
    display: flex;
    justify-content: space-between;
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
