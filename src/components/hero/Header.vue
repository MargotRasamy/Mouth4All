<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-color">
  <a class="navbar-brand" href="#"><img alt="logo" width="200" src="../../assets/logo.png"></a>
  <button class="navbar-toggler navbar-toggle" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
    <div class="navbar-nav">
      <a class="nav-item nav-link active" href="#">Notre vision<span class="sr-only">(current)</span></a>
      <a class="nav-item nav-link" href="#">Demo</a>
      <a class="nav-item nav-link" href="#">Soutenez-nous</a>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/variables/colors.scss";
@import "../../assets/variables/spaces.scss";
@import "../../assets/variables/medias.scss";
@import "../../assets/variables/misc.scss";
@import "../../assets/variables/reset.scss";


.bg-color {
  // background-color: var(--colorSecondaryLight);
}
.navbar {
  padding: var(--gutterWidth);
  position: fixed;
  width:100%;
  z-index: 1;
  display: flex;
  align-items: flex-end;
}


.navbar-toggle {
  border:0;
  outline:0;
}

.navbar-toggle:focus {
  outline: none !important;
}

</style>
