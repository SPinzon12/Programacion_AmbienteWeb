<template>
  <h1>Ejercicio 09</h1>
  <div> 
      <input type="number" v-model="columns" placeholder="Columnas" min="0">
      <br>
      <input type="number" v-model="rows" placeholder="Filas" min="0">
        <p v-if="columns > 0 && rows > 0">
          <table>
            <tbody>
              <tr v-for="row in rows">
                <td v-for="col in columns">{{row}},{{col}}</td>
              </tr>
            </tbody>
          </table>
        </p>

  </div>
</template>

<script>
export default {
  name: 'Tabla',
  data(){
      return{
          columns :'',
          rows: ''
      }
  }
}


</script>

<style scoped>
table {
font-family: 'Open Sans', sans-serif;
width: 750px;
border-collapse: collapse;
border: 3px solid #44475C;
margin: 10px 10px 0 10px;
}

table th {
text-transform: uppercase;
text-align: left;
background: #44475C;
color: #FFF;
padding: 8px;
min-width: 30px;
}

table td {
text-align: left;
padding: 8px;
border-right: 2px solid #7D82A8;
}
table td:last-child {
border-right: none;
}
table tbody tr:nth-child(2n) td {
background: #D4D8F9;
color: #0c155a
}



</style>