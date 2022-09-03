<template>
<h1> {{customTitle}}</h1>
<h2> {{n}} * {{n}} = {{multiplication}} </h2>
<button @click="increase">  +1 </button>
<button @click="decrease">  -1 </button>
<button @click="reset">  Reset </button>
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
    name: 'HelloWorld',
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

button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>
