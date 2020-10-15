<template>
  <a :href="path" class="button" :class="color">
      {{ text }}
  </a>
</template>

<script>

export default {
  name: "Button",
  props: [
      'text',
      'path',
      'color'
  ]
};
</script>

<style scoped lang="scss">
@import "../assets/variables/colors.scss";
@import "../assets/variables/spaces.scss";
@import "../assets/variables/medias.scss";
@import "../assets/variables/misc.scss";
@import "../assets/variables/reset.scss";

 .button {
    display: inline-block;
    border-radius: var(--borderRadiusSmall);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    min-width: max-content;
    padding: 0 var(--spaceS);
    height:45px;
    box-shadow: var(--boxShadow);
    font-weight: bold;
    margin: var(--spaceM) 0;
    cursor: pointer;
}

.button--primary {
    background-color: var(--colorPrimary);
    color: var(--colorWhite);
    box-shadow: var(--boxShadowPrimary);
    &:hover{
        background-color: var(--colorPrimaryLight);
        color: var(--colorWhite);
    }
}

.button--secondary {
    background-color: var(--colorSecondary);
    color: var(--colorWhite);
    box-shadow: var(--boxShadowSecondary);
    &:hover{
        background-color: var(--colorSecondaryLight);
        color: var(--colorWhite);
    }
}


</style>