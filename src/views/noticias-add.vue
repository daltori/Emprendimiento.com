<template>
<div class="row justify-content-center">
  
<div class="col-md-6">

    <h3 >Añadir Noticias</h3>
    <!-- <h3 >Post Edit</h3> -->
        <form @submit.prevent="crearformulario">

            <div class="form-group">
             <label >title</label>
            <input class="form-control" 
            type="text" 
            v-model="news.title"
            required>
            </div>
            <div class="form-group">
                <label >description</label>
               <textarea class="form-control" 
               type="text" 
               v-model="news.description"
                required> </textarea>
               </div>
               <div class="form-group">
                <label >Imagen</label>
               <input class="form-control" 
               type="text" 
               v-model="news.imagen"
                required
               >
               <!-- <img class="img-responsive" v-bind:src="{Imagen}"> -->
               <!-- <img class="responsive" v-bind:src="{Imagen}"> -->
               </div>


              
        <div class="form-group">
          <button class="btn btn-danger btn-block"  type="submit">Crear</button>
        </div>
               

        </form>
    
</div>

</div>
</template>

<script>
import axios from 'axios'
export default {
    
 data(){
    return{
      news:{
        title:"",
        description:"",
        imagen:""
      }
    }
  },
    methods:{
    crearformulario(){
      let apiURL="https://emprendimientovue.herokuapp.com/app/news/registrar"
      axios.post(apiURL,this.news)
      .then(()=>{
        this.$router.push("/")
        this.news={
        title:"",
        description:"",
        imagen:"",
      }
     
      })
       .catch((error)=>{
           console.log(error)
        
      })
    }
  }
}
</script>

<style>
input.ng-invalid.ng-touched,textarea.ng-invalid.ng-touched{

    border: 1px solid red;
}

</style>

