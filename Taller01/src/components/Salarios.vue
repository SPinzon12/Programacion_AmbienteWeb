<template>
    <div>
        <h1>Ejercicio 07</h1>

        <input @keypress.enter="salarios.push(salario)" type="number" v-model="salario" id="a" placeholder="Salarios (10)"> <br/>
        <br>
        <h2>{{salarios}}</h2>
        <button @click="newSal()"> +0.8% </button>
        <ul v-for="(salario, index) in nsalarios">
            <li> Salario {{index+1}}: ${{salario}} </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "Salarios",
    data(){
        return{
            salario: 0,
            salarios:[],
            nsalarios: []
        }
    },
    methods: {
        newSal(){
            if (this.salarios.length < 10){
                alert(`Por favor ingrese los salarios restantes: ${10-this.salarios.length}`);
            }
            else if(this.salarios.length > 10){
                alert("Por favor ingrese exactamente 10 salarios");
            }
            else if (this.salarios.length == 10){
                this.nsalarios = this.salarios.map(x => (x + x *0.8).toFixed(2));
            }
        }
    }
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
      background: rgba(0, 0, 0, 0.521);
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