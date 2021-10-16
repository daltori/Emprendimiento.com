<template>
  <div class="row justify-content-center">
    <div class="col-md-6">
      <h3 class="text-center">Iniciar sesion</h3>
      <form @submit.prevent="login(student)">
        <div class="from-group">
          <label>Email</label>
          <input
            type="text"
            class="form-control"
            v-model="student.email"
            required>

        </div>
        <div class="form-group mb-3">
          <label > Password</label>
          <input
            type="password"
            class="form-control"
            v-model="student.password"
            required
          >
        </div>
        <div class="alert alert-danger" role="alert">
          {{error}}

        </div>
        <div class="form-group">
          <button class="btn btn-danger btn-block">Login </button>

          </div>
      </form> 
    </div>

  </div>
</template>

<script>
import {mapActions,mapState}from 'vuex'

export default {
  data() {
    return{
      student:{
        email:'juan@gmail.com',
        password:'12345'
      },
      alerta:''
    }
    
  },
  methods:{
    ...mapActions(['login'])
  },
  computed:{
  ...mapState(['error'])
  }
}
</script>

<style>

</style>


