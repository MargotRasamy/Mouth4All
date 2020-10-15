<template>
  <div class="demos">
    <div class="caption">
        <Caption title="Donnez la voix à chacun." 
        content="Votre enfant pourra s'entraîner à parler afin de communiquer plus facilement avec le monde qui les entoure."/>
    </div>
    <div class="image">
        <span class="image-container">
            <img src="../../assets/images/mouthfront.gif" />
        </span>
    </div>
  </div>
</template>

<script>
import Caption from '../crowdfund/Caption'
export default {
  name: 'Demos',
  components: {
      Caption
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

.demos {
    display: flex;
    min-height: 100vh;
    @include small{
      flex-direction: column;
    }
    @include medium{
       flex-direction: column;
    }
}

.caption {
    width: 50%;
}

.image {
    background-color:black;
    width: 50%;
    display: flex;
    .image-container {
        width: 75%;
        margin: auto;
        img {
            width:100%;
            object-fit: cover;
    
            background-blend-mode:screen
            // mix-blend-mode: screen;
        }
    }
}

</style>
