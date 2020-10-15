<template>
  <div class="mouth">
    <div class="webgl"></div>
  </div>
</template>

<script>
import * as THREE from 'three'
// import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls'
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader'


export default {
  name: 'HelloWorld',
  data () {
    return {
      container: null,
      scene: null,
      camera: null,
      controls: null,
      renderer: null
    }
  },
  methods: {
    init () {
      // set container
      this.container = document.querySelector('.webgl')

      // add camera
      var camera = new THREE.PerspectiveCamera(70, 
      window.innerWidth/window.innerHeight, 0.1, 1000 ); // Specify camera type like this
      camera.position.set(0,0,5); // Set position like this
      camera.lookAt(new THREE.Vector3(0,0,0));
      this.camera = camera

      // create scene
      this.scene = new THREE.Scene()

      // this.scene.background = new THREE.Color('none')

      // add lights
      const ambientLight = new THREE.HemisphereLight(
        0xffffff, // bright sky color
        0x222222, // dim ground color
        1 // intensity
      )
      const mainLight = new THREE.DirectionalLight(0xffffff, 4.0)
      mainLight.position.set(10, 10, 10)
      this.scene.add(ambientLight, mainLight)

      // add controls
      // this.controls = new OrbitControls(this.camera, this.container)

      // create renderer
      this.renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true })
      this.renderer.setSize(this.container.clientWidth, this.container.clientHeight)
      this.renderer.setPixelRatio(window.devicePixelRatio)
      // this.renderer.gammaFactor = 2.2
      // this.renderer.outputEncoding = THREE.sRGBEncoding
      // this.renderer.physicallyCorrectLights = true
      this.container.appendChild(this.renderer.domElement)
      // this.renderer.setClearColor( 0x000000, 0 );
      // set aspect ratio to match the new browser window aspect ratio
      this.camera.aspect = this.container.clientWidth / this.container.clientHeight
      this.camera.updateProjectionMatrix()
      this.renderer.setSize(this.container.clientWidth, this.container.clientHeight)

      const loader = new GLTFLoader()

      loader.load(
        '/models/Girl.gltf',
        gltf => {
          this.scene.add(gltf.scene)
        }
      )

      this.renderer.setAnimationLoop(() => {
        this.render()
      })
    },
    render () {
      this.renderer.render(this.scene, this.camera)
    }
  },
  mounted () {
    this.init()
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

.mouth {
    min-height: 100vh;
    display: flex;
}
.webgl {    width: 40rem;    height:30rem;
outline: none !important;
margin: auto;  }


</style>