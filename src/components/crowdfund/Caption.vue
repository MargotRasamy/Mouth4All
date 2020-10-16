<template>
  <div class="caption">
    <h2>{{ title }}</h2>
    <p v-if="content">{{ content }}</p>
    <p class="content3" v-if="content3"> {{ content3 }}</p>
    <p class="content2" v-if="content2"> {{ content2 }}</p>
    <a class="link" v-if="link" href="www.google.com" target="_blank">www.ulule.com/Mouth4All</a>
    <!-- <span class="cta">
        <Button text="Soutenez-nous" path="#video" color="button--primary"/>
        <Button text="Voir la vidéo" path="#video" color="button--secondary"/>
    </span> -->
  
  </div>
</template>

<script>
export default {
  name: 'Caption',
  props: [
      'title',
      'content',
      'link',
      'content2',
      'content3'
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/variables/colors.scss";
@import "../../assets/variables/spaces.scss";
@import "../../assets/variables/medias.scss";
@import "../../assets/variables/misc.scss";
@import "../../assets/variables/reset.scss";

.link {
  word-wrap: break-word;
  @include small{
      font-size: 1.4rem;
    }
    @include medium{
       font-size: 1.6rem;
    }
}
a {
    text-decoration: none;
    font-size: 1.8rem;
    color: var(--colorWhite);
}
.caption {
  
  list-style-type: space-counter;
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

.content2, .content3{
  display:list-item;
  list-style-position: inside;
  margin-top: 1rem;
  list-style: "\1F3B2";
  padding-left: 1rem;
  margin-left: 1rem;
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