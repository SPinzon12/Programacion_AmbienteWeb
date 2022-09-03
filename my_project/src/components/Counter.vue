<template>
    <h1> {{customTitle}}</h1>
    <br>
    <h2> {{n}} * {{n}} = {{multiplication}} </h2>
    <br>
    <button @click="increase">  +1 </button>
    <button @click="decrease">  -1 </button>
    <button @click="reset">  Reset </button>
    <br>
    <h2>{{start}}</h2>
</template>


<script>
      export default {
        props: {
          title: String,
          start: {
            type: Number,
            default: 10,
            requiered: false,
            validator: (value) => {
              return value >= 0
            }
    
          }
        },
        name: 'Counter',
        data () {
          return{
            n: 5
          }
        },
        methods: {
          increase(){
            this.n ++;
            console.log(this.n);
          },
          decrease(){
            this.n --;
    
          },
          reset(){
            this.n =  5
            console.log(this.n)
          }
        },
        computed: {
          multiplication(){
            console.log('calling method');
            return this.n * this.n
          },
          customTitle(){
            
            return this.title ?? 'MY COUNTER'
    
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