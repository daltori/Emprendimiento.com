<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div class="c-anim__item js-anim-container">

    </div>
    
  </div>
</template>
<script>
const anim= document.querySelectorAll('.js-anim-container')
import anim_json from "../assets/boy.json"
import lottie from "../../node_modules/lottie-web/build/player/lottie";
lottie.loadAnimation({
  container: anim,
  render: 'svg',
  loop:true,
  autoplay:true,
  animationData:anim_json

})
export default{
  name:'about',

}
</script>
