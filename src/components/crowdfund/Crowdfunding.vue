<template>
    <div class="crowdfunding">
        <Caption />
        <Footer />
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
   
}




</style>