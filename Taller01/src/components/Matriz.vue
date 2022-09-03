<template>
    <div> 
        <h1>Ejercicio 10</h1>
        <input type="number" v-model="rows" placeholder="Filas" min="0">
        <button @click="create" v-if="columns > 0 && rows > 0" > Create </button>
        <br>
        <input type="number" v-model="columns" placeholder="Columnas" min="0" @keyup="sum=new Array(columns)">
        <button @click="suma" v-if="columns > 0 && rows > 0" > Sumar </button>
          <p>
            <table>
              <tbody>
                <tr v-for="(row,i) in rows">
                    <td v-for="(col,j) in columns">
                        <input type="number" placeholder="Valor" min="0" @keyup="add($event,i,j)">
                    </td>
                </tr>
                <tr v-if="sum[sum.length-1]!=null">
                  <td v-for="(col,i) in columns"> {{sum[i]}}</td>
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
            rows: '',
            matrix: [],
            sum: [],
            
        }
    },
    methods: {
        create(){
            this.matrix = new Array(this.rows);
            for (let i = 0; i < this.rows; i++) {
                this.matrix [i] = new Array(this.columns)
                
            }
        },
        add(event,i,j){
          this.matrix[i][j]= parseInt(event.target.value);
        },
        suma(){
        for (let col = 0; col < this.matrix[0].length; col++) {
            let sumCol = 0;
            for (let row = 0; row < this.matrix.length; row++) {
              sumCol+= this.matrix[row][col];              
            }
          this.sum[col]= sumCol; 
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
  
</style>