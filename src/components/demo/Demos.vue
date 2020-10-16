<template>
  <div class="demos">
    <div class="caption-container">
        <Caption title="Donnez une voix à chacun." 
        content="Vos enfants pourront entraîner leur élocution afin de communiquer plus facilement avec le monde qui les entoure. Offrez-leur le choix et l'opportunité d'exprimer leurs rêves et maximisez leurs chances de s'épanouir en milieu social."/>
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
    align-items: center;
    min-height: 100vh;
    @include small{
      flex-direction: column;
    }
    @include medium{
       flex-direction: column;
    }
}

.caption-container {
    margin: 0 auto;
    width: 50%;
    @include small{
      width: 90%;
    }
    @include medium{
       width: 90%;
    }
}

.image {
    background-color: black;
    width: 50%;
    display: flex;
    margin: auto;
    @include small{
      width: 90%;
    }
    @include medium{
       width: 90%;
    }
    .image-container {
        width: 75%;
        margin: auto;
        img {
            width:100%;
            object-fit: cover;
            // mix-blend-mode: screen;
            //background-blend-mode:screen;
           
        }
    }
}

</style>
