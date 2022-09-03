<template>
  <h1> Ejercicio 02</h1>
  <div>
    <input type="text" v-model="call" placeholder="Duración Llamada (mins)" min="0">
    <br>
    <h2>{{pagar}}</h2>
  </div>
</template>

<script>
  export default{
    name: 'Llamada',
    data () {
        return {
            call: ''
          }      
    },
    computed: {
      pagar(){
       
        return `Total a pagar: $${(this.call<3) ? 100 : 50*(this.call-3)+100}`
       
      }
    }
    
  }
</script>



<style scoped>
  h1 {
    font-weight: 500;
    font-size: 2.6rem;
    top: -10px;
  }

  h3 {
    font-size: 1.2rem;
  }

  .greetings h1,
  .greetings h3 {
    text-align: center;
  }

  @media (min-width: 1024px) {
    .greetings h1,
    .greetings h3 {
      text-align: left;
    }
  }

  input {
    position: absolute;
    font-size: 16px;
    color: #b8b8b8;
    border-radius: 5px;
  }

</style>

