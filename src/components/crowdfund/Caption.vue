<template>
  <div class="caption">
    <h2>Aidez-nous à aider les autres</h2>
    <p>En soutenant notre innovation technologique, vous nous aiderez à rendre le quotidien des enfants atteints de déficience auditives plus agréable. Que vous soyez concerné ou non, si notre projet vous tient à cœur, soutenez-nous :</p>
    <a href="www.google.com" target="_blank">www.ulule.com/Mouth4All</a>
    <!-- <span class="cta">
        <Button text="Soutenez-nous" path="#video" color="button--primary"/>
        <Button text="Voir la vidéo" path="#video" color="button--secondary"/>
    </span> -->
    
  </div>
</template>

<script>
export default {
  name: 'Caption'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/variables/colors.scss";
@import "../../assets/variables/spaces.scss";
@import "../../assets/variables/medias.scss";
@import "../../assets/variables/misc.scss";
@import "../../assets/variables/reset.scss";


a {
    text-decoration: none;
    font-size: 1.8rem;
    color: rgb(0, 157, 255);
}
.caption {
  margin: 5vh auto;
    width: 70%;
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

h2 {
    font-family: DMSansBold;
    font-size: 2.4rem;
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