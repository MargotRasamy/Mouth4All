<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-color">
    <a class="navbar-brand" href="#"><img alt="logo" width="200" src="../../assets/logo.png"></a>
    <button class="navbar-toggler navbar-toggle" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-item nav-link active" href="#">Notre vision<span class="sr-only">(current)</span></a>
        <a class="nav-item nav-link" href="#demo">Vidéo</a>
        <a class="nav-item nav-link" href="#crowd">Soutenez-nous</a>
        
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'Header',
  mounted() {
    const links = document.querySelectorAll('.nav-item')
     
    for(let i = 0 ; i< links.length ; i ++) {
      links[i].addEventListener('click',
      () => {
        Array.from(links, link => link.classList.remove('active'));
        links[i].classList.add('active');
      })
    }
      
    
    
      
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


.navbar {
  padding: var(--spaceM) var(--gutterWidth);
  width:100%;
  background-color: rgba(250,250,250, 0.95);
  
  display: flex;
  align-items: flex-end;
  position: fixed;
  z-index: 9;
  
}
.active {
  color: var(--colorPrimary) !important;
}

.navbar-toggle {
  border:0;
  outline:0;
}

.navbar-toggle:focus {
  outline: none !important;
}

</style>
