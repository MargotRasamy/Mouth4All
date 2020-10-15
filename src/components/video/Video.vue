<template>
  <div class="video-section">
    <span class="video-wrap" @click="play">
        <a alt="btn" class="play"><img src="../../assets/images/play-button.svg" alt="play-button" /> </a>
        <video src="../../assets/videos/vid.mp4" controls />
    </span>
  </div>
</template>

<script>
export default {
  name: 'Video',
  methods: {
      play() {
        const video = document.querySelector('video')
        const btn = document.querySelector('.play')
            btn.classList.toggle('invisible')
            video.play()
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

.video-section {
    min-height: 100vh;
    display: flex;
}
.video-wrap {
    padding: 0;
    display: flex;
    margin: auto;
    box-shadow: var(--boxShadow);
    border-radius: var(--borderRadiusMedium);
    position: relative;
    outline: none;

    a {
        cursor: pointer;
        position: absolute;
        z-index: 1;
        width: 5rem;
        height: 5rem;
        right: calc(50% - 2.5rem);
        top: calc(50% - 2.5rem);
        opacity: 0.7;
    }
    img {
        width: 100%;
        object-fit: cover;
        cursor: pointer;
    }
}

.invisible {
    display: none;
}
video {
    border-radius: var(--borderRadiusMedium);
    margin: auto;
    padding: 0;
    background-color: black;
    outline: none;
    width: 80vw;
    height: 80vh;
    @include small{
      height: 50vh;
    }
    @include medium{
       height: 70vh;
    }
}

</style>
