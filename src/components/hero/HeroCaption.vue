<template>
  <div class="hero-caption">
    <h1>Mouth4All</h1>
    <p>La nouvelle Web App qui permet aux sourds et malentendants de s'intégrer plus facilement dans les écoles, en apprenant la prononciation grâce à une bouche 3D qui mime le mouvement des lèvres. </p>
    <span class="cta">
        <Button text="Soutenez-nous" path="#video" color="button--primary"/>
        <Button text="Voir la vidéo" path="#video" color="button--secondary"/>
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
    padding: var(--spaceXL);
    @include small{
      width: 100%;
      padding: var(--spaceM);
    }
    @include medium{
      width: 100%;
      padding: var(--spaceM);
    }
}

@font-face {
  font-family: 'DMSansBold';
  src: url("../../assets/fonts/DM_Sans/DMSans-Bold.ttf");
}

h1 {
    font-family: DMSansBold;
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