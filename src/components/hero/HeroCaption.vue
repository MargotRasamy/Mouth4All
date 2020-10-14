<template>
  <div class="hero-caption">
    <h1>Mouth4All</h1>
    <p>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.</p>
    <span class="cta">
        <Button />
        <Button />
    </span>
    
  </div>
</template>

<script>
import Button from '../Button.vue'
export default {
  name: 'HeroCaption',
  components: {
      Button
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

.hero-caption {
    width: 50%;
    padding: var(--spaceM);
    @include small{
      width: 100%;
    }
    @include medium{
      width: 100%;
    }
}

h1 {
    margin-bottom: var(--spaceS);
}
.cta {
    display: flex;
    margin: var(--spaceS) 0;
    & .button {
      width: 50px;
      padding: var(--spaceM);
    }
    & .button:first-of-type {
      margin-right: var(--spaceS);
    }
    
}


</style>