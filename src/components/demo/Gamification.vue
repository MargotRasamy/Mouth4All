<template>
    <div class="gamification">
        <div class="image">
            <span class="image-container">
                <img src="../../assets/images/map.jpg" />
            </span>
        </div>
        <div class="caption-container">
            <Caption title="Apprendre des mots sous la forme d'un jeu d’aventure" 
            content2="Quêtes pour compléter 3 sessions sur un thème de vocabulaire."
            content3="A chaque niveau passé, de nouvelles sections de mots et de nouveaux accessoires pour l’avatar sont débloqués."
            />
        </div>
        
    </div>
</template>

<script>
import Caption from '../crowdfund/Caption'

export default {
  name: 'Gamification',
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
      flex-direction: column-reverse;
    }
    @include medium{
       flex-direction: column-reverse;
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
        width: 75%;
        margin: auto;
        @include small{
        width: 80%;
        }
        @include medium{
        width: 65%;
        }
        img {
            width:100%;
            object-fit: cover;
    
            background-blend-mode:screen
            // mix-blend-mode: screen;
        }
    }
}

</style>