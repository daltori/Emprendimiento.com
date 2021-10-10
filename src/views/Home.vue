<template>
  <div>
    <carrucel></carrucel>
    
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Carrucel from '../components/Carrucel.vue'


export default {
  name: 'Home',
  components: {
    HelloWorld,
    Carrucel
  }
}
</script>
