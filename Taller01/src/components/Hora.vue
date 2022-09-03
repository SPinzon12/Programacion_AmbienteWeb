<template>
  <h1>Ejercicio 01</h1>
  <div>
    <input type="text" v-model="sec" placeholder="Hora en segundos">
    <br>
    <br>
    <h2>{{convertir}}</h2>
  </div>

</template>

<script>
  export default{
    name: 'Hora',
    data () {
        return {
            sec: ''
          }      
    },
    computed: {
      convertir(){
        
        return `${Math.floor(this.sec/3600)} horas, ${Math.floor(this.sec/60)%60} minutos y ${Math.round(this.sec)%60} segundos.`
      }
    },
    
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
  top: 10px;
  left: 8px;
  font-size: 16px;
  color: #b8b8b8;
  border-radius: 5px;
}

button {
  display: inline-block;
  padding: 12px 18px;
  cursor: pointer;
  border-radius: 5px;
  background-color: #8ebf42;
  font-size: 16px;
  font-weight: bold;
  color: #fff;
}
</style>

