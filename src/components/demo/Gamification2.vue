<template>
    <div class="gamification">
        <div class="caption-container">
            <Caption title="Un concept ludique qui favorise la progression" 
            content2="Carte de progression à la Candy Crush : chaque niveau correspond à une section de mots (champ lexicaux, prépositions…)."
            content3="Avatar personnalisable par le joueur."
            />
        </div>
        <div class="image">
            <span class="image-container">
                <img src="../../assets/images/cards.png" />
            </span>
        </div>
    </div>
</template>

<script>
import Caption from '../crowdfund/Caption'

export default {
  name: 'Gamification2',
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


.gamification {
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
        width: 50%;
        margin: auto;
     @include small{
      width: 70%;
    }
    @include medium{
       width: 60%;
    }
        img {
        
            width: 100%;
            object-fit: cover;
    
            background-blend-mode:screen
            // mix-blend-mode: screen;
        }
    }
}

</style>