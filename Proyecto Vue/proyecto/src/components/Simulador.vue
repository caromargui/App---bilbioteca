<template>
  <v-container>
    <v-row >
      <v-col class="text-center">
        <h1>Simulador de crédito</h1>
    </v-col>
    </v-row>
    <v-row>
      <v-col class="text-center">
        <v-text-field
          type="number"
          label="Valor del préstamo"
          :rules="rules1"
          hide-details="auto"
          v-model="valorprestamo"
        ></v-text-field>
        <v-text-field
          type="number"
          label="Interes mensual efectivo (%)"
          :rules="rules3"
          hide-details="auto"
          v-model="interes"
        ></v-text-field>
        <v-text-field
          type="number"
          label="Cantidad de cuotas"
          :rules="rules2"
          hide-details="auto"
          v-model="cuotas"
        ></v-text-field>
      </v-col>
      <v-col>
       <v-card
          class="mx-auto"
          max-width="400"
       >
       <v-img
         src="https://como-funciona.com/wp-content/uploads/2020/11/creditos-de-nomina-800x400.jpg"
         height="200px"
       ></v-img>   
       </v-card>  
      </v-col>
    </v-row>
    <v-row>
      <v-col class="text-center">
      <v-btn
          color="primary"
          elevation="2"
          rounded
          medium
          @click="cuotafija"
      >Simular </v-btn>
      </v-col>
    </v-row>
    <v-row>
    <v-col></v-col>
    <v-col class="text-center" 
      v-for="n in 1"
      :key="n"
      cols="6"><v-card
      class="pa-1"
      elevation="6"
      outlined
      style="background-color: lightgray;"
      shaped>
    <h3>Valor Cuota</h3>
    <h4>{{(valorcuota)}}
           </h4></v-card></v-col>
    <v-col></v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
    name: "SimuladorCredito",
    data: () => {
      return {
        valorprestamo:null,
        cuotas:null,
        valorcuota:"",
        i:"",
        rules1:[
          value => !!value||'Valor obligatorio',
          value => (value && value >= 1000000)||'Valor obligatorio mayor a $1.000.000'
        ],
        rules2:[
          value => !!value||'Cantidad de cuotas es un valor obligatorio',
          value => (value && value >= 12 && value <=120)||'La cantidas de cuotas debe ser mayor mayor a 12 y menor a 120'
        ],
        rules3:[
          value => !!value||'Tasa anual efectiva es obligatoria',
          value => (value && value <=30)||'La TAE no puede ser mayor a la tasa de usura '
        ],
        
      };
  },
  methods: { 
      cuotafija(){
        this.i=parseFloat(this.interes)/100.0
     //solucion sencilla<!---this.valorcuota=((parseFloat(this.valorprestamo))*(parseFloat(this.interes)))/(1-(1+(parseFloat (this.interes)))^(parseFloat(this.cuotas)*-1));
      this.valorcuota=(parseFloat(this.valorprestamo)*(this.i))/(1-((1+this.i))**(-parseFloat(this.cuotas)))
      //this.valorcuota=((parseFloat(this.valorprestamo)|| 0*(1+((parseFloat(this.interes))|| 0/100)))^(parseFloat(this.cuotas))|| 0/parseFloat(this.cuotas)).toFixed(2);
       if (isNaN(valorprestamo) || isNaN(interes) || isNaN(cuotas)) {
       valorcuota = '0';
        return;}
      //<!---(0,796575374*((1+0,796575374)^(parseFloat (this.cuotas)))))/(((1+0,796575374)^(parseFloat(this.cuotas)))-1);
    }

  },
} 
</script>

<style>

</style>