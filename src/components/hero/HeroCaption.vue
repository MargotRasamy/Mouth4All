<template>
  <div class="hero-caption">
    <h1>Mouth4All</h1>
    <p>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. </p>
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
  margin-top: 0;
    width: 50%;
    padding: var(--spaceL);
    @include small{
      width: 100%;
    }
    @include medium{
      width: 100%;
    }
}

h1 {
    font-size: 4.8rem;
    margin-bottom: var(--spaceS);
    color: var(--colorSecondary);
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
    @include small{
      display: grid;
      grid-template-columns: repeat(2, auto);
      grid-column-gap: 2vh;
      & .button {
      width: 100%;
      padding: var(--spaceM);
    }
    & .button:first-of-type {
      margin-right: 0;
    }
    }
    @include medium{
      display: grid;
      grid-template-columns: repeat(2, auto);
      grid-column-gap: 2vh;
      & .button {
      width: 100%;
      padding: var(--spaceM);
    }
    & .button:first-of-type {
      margin-right: 0;
    }
    }
}


</style>