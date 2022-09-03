
<template>
  <!-- <HelloWorld title='TOF'></HelloWorld>
  <br>
  <HelloWorld :start="15"></HelloWorld> -->
  <!-- <Directives></Directives> -->
  <Indecision ></Indecision>
    
</template>

<script>
  import HelloWorld from '@/components/HelloWorld.vue';
  import Directives from '@/components/Directives.vue';
  import Indecision from '@/components/Indecision.vue';

  export default{
    name: 'App',
    components: {
    HelloWorld,
    Directives,
    Indecision
}
} 
  </script>
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
</style>
