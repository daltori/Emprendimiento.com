<template>
  <div>
    <carrucel></carrucel>
    <h2>Noticias</h2>
    <div class=" d-flex flex-row pt-4">

    <Noticias class="col-md-6 col-12"></Noticias>
    <Noticias class="col-md-6  col-12"></Noticias>
    
    </div>
    <div class=" d-flex flex-row pt-4">

    <Noticias class="col-md-6 col-12"></Noticias>
    <Noticias class="col-md-6  col-12"></Noticias>
    
    </div>
    
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Noticias from '@/components/Noticias.vue'
import Carrucel from '../components/Carrucel.vue';




export default {
  name: 'Home',
  components: {
    HelloWorld,
    Carrucel,Noticias
  }
}
</script>
