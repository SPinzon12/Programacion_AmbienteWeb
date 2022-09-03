<template>
    <Div>
        <h1>Ejercicio 06</h1>
        <br>
        <input @keypress.enter="impares()" type="number" v-model="n" placeholder="Número">
        <br>
        <h4>{{imp}}</h4>
    </Div>
</template>


<script>
  export default{
    name: 'Impares',
    data(){
      return {
          n: '',
          imp: []
        }
      },
      methods: {
          impares(){
            for (let i = 0; i < this.n; i++) {
              i%2 == 0 ? null : this.imp.push(i)
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