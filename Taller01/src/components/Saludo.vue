<template>
    <h1>Ejercicio 03</h1>
    <div>
        <input type="text" v-model="name" placeholder="Nombre">
        <br>
        <input type="text" v-model="hour" placeholder="Formato 24h" min="0" max="23">
        <br>
        <br>
        <p v-if="hour < 23"> 
          <button @click="saludo">Saludar</button>
          <br>
          <h1>{{greeting}}</h1>
        </p>
        <p v-else> Hora no Valida </p>
            
    </div>
</template>

<script>
export default {
    name: 'Saludo',
    data(){
        return{
            hour:'',
            name:'',
            greeting:''
        }
    },methods:{
        saludo(){
            if (this.hour<12){
                this.greeting = `Buenas días, ${this.name}`

            }
            else if(this.hour >=12 && this.hour<19){
                this.greeting = `Buenas tardes, ${this.name}`
            }
            else{
                this.greeting = `Buenas noches, ${this.name}`
            }
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