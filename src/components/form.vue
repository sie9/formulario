<template>
  <div class="form" v-bind:class="{'input-field': info.isMaterialize, 'container': info.isBoostrap}">
    <label v-if="info.username">Usuario: </label>
    <input type="text" v-if="info.username" v-model="usuario.username" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.email">Email: </label>
    <input type="email" v-if="info.email" v-model="usuario.email" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.tel">Telefono: </label>
    <input type="number" v-if="info.tel" v-model="usuario.tel" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.pass">Contraseña: </label>
    <input type="password" v-if="info.pass" v-model="usuario.pass" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.time">Hora: </label>
    <input type="time" v-if="info.time" v-model="usuario.time" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.color">Color: </label>
    <input type="color" v-if="info.color" v-model="usuario.color" v-bind:class="{'form-control': info.isBoostrap}">
    <label v-if="info.date">Fecha: </label>
    <input type="date" v-if="info.date" v-model="usuario.date" v-bind:class="{'form-control': info.isBoostrap}">
  </div>
</template>

<script>
export default {
  name: 'formulario',
  props: ['info'],
  data() {
    return {
        usuario:{
          username:"",
          email:"",
          tel:"",
          pass:"",
          time: "",
          color:"",
          date:""
        }
    }
  },
  watch:{
    usuario: {
      handler:function(){
        console.log(this.usuario);
        this.$emit('usuario',JSON.stringify(this.usuario,null,2));
      },
      deep:true
    }
  }
}
</script>

<style lang="css">

input[type="date"] {
  display: flex;
    align-items: center;
}
</style>
