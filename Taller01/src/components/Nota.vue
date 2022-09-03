<template>
    <Div>
        <h1>Ejercicio 11</h1>
        <input type="text" v-model="student.name" placeholder="Nombre">
        <br>
        <input type="text" v-model="student.n1" placeholder="Nota 1">
        <br>
        <p v-if="student.n1<=5">
            <input type="text" v-model="student.n2" placeholder="Nota 2">
            <br>
        </p>
        <p v-else> Las notas van hasta 5</p>
        <p v-if="student.n2<=5">
            <input type="text" v-model="student.n3" placeholder="Nota 3">
            <br>
        </p>
        <p v-else> Las notas van hasta 5</p>
        <button @click="approve()"> ¿Gano o Perdio la Materia? </button>
        <br>
        <h1>{{student.ans}}</h1>
    </Div>
</template>


<script>
  export default{
    name: 'Nota',
    data(){
      return {
        student:{
            name: '',
            n1: '',
            n2: '',
            n3: '',
            avg: '',
            ans: ''
        }
  
      }
    },
    methods:{
        approve(){
            this.student.avg = (parseFloat(this.student.n1)+parseFloat(this.student.n2)+parseFloat(this.student.n3))/3;
            this.student.avg = this.student.avg.toFixed(2);
            if(this.student.avg >= 3){
                this.student.ans = `${this.student.name}: Gano la materia`
            }
            else if(this.student.avg < 3, this.student.avg >= 0){ 
                this.student.ans = `${this.student.name}: Perdio la materia`
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