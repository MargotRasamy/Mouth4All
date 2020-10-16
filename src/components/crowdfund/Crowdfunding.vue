<template>
    <div class="crowdfunding">
        <Caption link="true" title="Aidez-nous à aider les autres"
        content="En soutenant notre innovation technologique, vous nous aiderez à rendre le quotidien des enfants atteints de déficiences auditives plus agréable. Que vous soyez concerné ou non, si notre projet vous tient à cœur, soutenez-nous :" />
        <Footer />
        <img class="phone" src="../../assets/images/phone.png" alt="phone" />
    </div>
</template>

<script>
import Caption from './Caption'
import Footer from '../footer/Footer'

export default {
  name: 'Crowdfunding',
  components: {
      Caption,
      Footer
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

.crowdfunding {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    position: relative;
    & .caption {
       @include small{
    padding: 0 2rem;
    }
    @include medium{
     padding: 0 2rem;
    } 
    }
   
}

.phone {
    position: absolute;
    z-index: 2;
    right: 2vw;
    top: 5vh;

     @include small{
    display: none;
    }
    @include medium{
     display: none;
    }
    @include large{
     display: none;
    }
}


</style>