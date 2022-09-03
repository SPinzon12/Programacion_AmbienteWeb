<template>
<input type="text" v-model="newMessage" placeholder="Mensaje">
<br>
<input type="text" v-model="newAuthor" placeholder="Autor">
<br>
<button @click="addQuote">Continuar</button>
<br>
<ul>
    <li v-for="(item,index) in items">
       <span>{{index+1}}. {{item.mensaje}}</span> 
       <span v-if="item.author"> Por {{item.author}}</span>
       <span v-else> No author</span>
       <span v-show="item.mensaje"> Por {{item.author}}</span>


    </li>
</ul>

</template>

<script>
  export default {
    name: 'Directives',
    data(){
        return{
            newMessage:'',
            newAuthor:'',
            items: [
            {mensaje: 'Foo', author: 'Juan'},
            {mensaje: 'Bar', author: 'Pedro'}
        ]

        }
    },
    methods: {
      addQuote(){
        return this.items.unshift({
          mensaje:this.newMessage,
          author: this.newAuthor
          })
      }}
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
