<template>
  <div class="container">
    <table class="table table-success table-striped mt-5">
  <thead>
    <tr>
      <th scope="col">Nombre</th>
      <th scope="col">Email</th>
      <th scope="col">Telfono</th>
      <th scope="col">Acciones</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="student in students" :key="student._id">
      <td>{{student.name}}</td>
      <td>{{student.email}}</td>
      <td>{{student.phone}}</td>
      <td>
        <button class="btn btn-danger" @click.prevent="eliminarStudent(student._id)">Eliminar</button> |
        <router-link  class="btn btn-warning" :to="{name: 'Editar', params:{id:student._id}}"> Editar </router-link>
        
      </td>
      
    </tr>
    
  </tbody>
</table>
  </div>
</template>

<script>
// @ is an alias to /src


import  axios from 'axios';
export default {
  name: 'Home',
  data(){
    return{
      students: [],
    }
  },
  created(){
    let apiURL="https://emprendimientovue.herokuapp.com/api/api"
    axios.get(apiURL)
    .then((res)=>{
      this.students=res.data;
    })
    .catch((error)=>{
      console.log(error);
    })
  },
  methods:{
    eliminarStudent(id){
      let apiURL=`https://emprendimientovue.herokuapp.com/api/delete-student/${id}`
      let indexOfArrayItem= this.students.findIndex((i)=>i._id==id)
      if(window.confirm("esta seguro de elliminar el dato")){
      axios.delete(apiURL)
      .then((res)=>{
        this.students.splice(indexOfArrayItem,1)
        console.log(res)
      })
      .catch((error)=>{
        console.log(error)
      })
    }
    }
  },
 
}
</script>
