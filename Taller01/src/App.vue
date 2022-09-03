<script>
  import Hora from '@/components/Hora.vue';
  import Llamada from '@/components/Llamada.vue';
  import Tabla from '@/components/Tabla.vue';
  import Matriz from '@/components/Matriz.vue';
  import Saludo from '@/components/Saludo.vue';
  import Aleatorio from '@/components/Aleatorio.vue';
  import Numeros from '@/components/Numeros.vue';
  import Lista from '@/components/Lista.vue';
  import Nota from '@/components/Nota.vue';
  import Notas from '@/components/Notas.vue';
  import Impares from '@/components/Impares.vue';
  import Salarios from '@/components/Salarios.vue';
  






  export default{
    name: 'App',
    components: {
    Hora,
    Llamada,
    Tabla,
    Matriz,
    Saludo,
    Aleatorio,
    Numeros,
    Lista,
    Nota,
    Notas,
    Impares,
    Salarios,
}
} 
</script>


<template>
  <!-- <Hora></Hora> -->
  <!-- <Llamada></Llamada> -->
  <!-- <Saludo></Saludo> -->
  <!-- <Numeros></Numeros> -->
  <!-- <lista></lista> -->
  <!-- <Aleatorio></Aleatorio>  -->
  <!-- <tabla></tabla> -->
  <!-- <Matriz></Matriz> -->
  <!-- <Nota></Nota> -->
  <!-- <Notas></Notas> -->
  <!-- <Impares></Impares> -->
  <Salarios></Salarios>
</template>



<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
.fade-in {
  animation: fadeIn;
  animation-duration:.5s;
}
</style>
