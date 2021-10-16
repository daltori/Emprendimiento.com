<template id="animacion">
    <div >
        <lottie :options="defaultOptions" :height="200" :width="200" :view=true v-on:animCreated="handleAnimation"/>
    
    </div>
</template>
 
<script>
  import Lottie from "../../node_modules/vue-lottie/src/lottie.vue";
  import * as animationData from '../assets/monster.json';
 
  export default {
    name: 'animacion',
    components: {
      'lottie': Lottie
    },
    data() {
      return {
        defaultOptions: {animationData: animationData},
        animationSpeed: 1
      }
    },
    methods: {
      handleAnimation: function (anim) {
        this.anim = anim;
      },
 
      stop: function () {
        this.anim.stop();
      },
 
      play: function () {
        this.anim.play();
      },
 
      pause: function () {
        this.anim.pause();
      },
 
      onSpeedChange: function () {
        this.anim.setSpeed(this.animationSpeed);
      }
    }
  }
</script>
 