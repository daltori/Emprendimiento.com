<template>
 <div class=" py-5 bg-dark " >
      <div class="d-flex flex-wrap ">
        <div class="col-12 col-md">
          <img src="../../img/Logo.png">
          <small class="d-block mb-3 text-muted">© 2021</small>
        </div>
        <div class="col-4 col-md">
          <h5 class="text-light">Features</h5>
          <p>El emprendimiento en épocas de crisis a sido la mejor manera de poder impulsar la economía mundial ,creando empresas nuevas de manera que su mayor prioridad son los nuevos retos,la redes sociales juegan un papel importante.una nueva manera de poder emprender llevando la información a través de la red impulsando nuevos modelos de negocios en la industria 4.0</p>
        </div>
        <div class="col-4 col-md">
          <h5 class="text-light">Resources</h5>
          <ul class="list-unstyled text-small">
            <li><router-link class="text-muted" to="/">Home</router-link></li>
            <li><router-link class="text-muted" to="/about">Servicios</router-link></li>
            <li><a class="text-muted" href="#">Another resource</a></li>
            <li><a class="text-muted" href="#">Final resource</a></li>
          </ul>
        </div>
        <div  class="col-4 col-md">
          <animacion></animacion>
        </div>
        
      </div>
      </div>
</template>

<script>
 import animacion from '@/components/animacion.vue'
  export default {
    name: 'footer',
    components: {
    
    animacion
  }};
</script>