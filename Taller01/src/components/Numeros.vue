<template>
    <h1>Ejercicio 04</h1>
    <div> 
        <input type="number" v-model="n1" placeholder="Número 1">
        <br>
        <input type="number" v-model="n2" placeholder="Número 2">
        <br>
        <input type="number" v-model="n3" placeholder="Número 3">
        <br>
        <p>
            <button @click="numbers"> Iguales?</button>
            <h2>Hay {{equal}} números iguales.</h2>
        </p>

    </div>
</template>
  
<script>
  export default {
    name: 'Numeros',
    data(){
        return{
            n1: '',
            n2: '',
            n3: '',
            equal: ''

        }
    },
    methods: {
        numbers(){
            if (this.n1 == this.n2 && this.n2 == this.n3){
                this.equal = 3;
            }
            else {
                if (this.n1 == this.n2){
                    this.equal = 2;
                    }
                else if (this.n1 == this.n3){
                    this.equal = 2;
                    }
                else if (this.n2 == this.n3){
                    this.equal = 2
                }
                else {
                     this.equal = 0
                }    
            }
        }

    },
  }
</script>
  
<style scoped>
  table, th, td {
  border: 1px solid;
  } 
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
  button {
    background: black;
    color: #fff;
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -ms-border-radius: 5px;
    -o-border-radius: 5px;
    outline: none;
    padding: 0.7rem 2rem;
    border: none;
    margin-top: 2rem;
  }

  
</style>