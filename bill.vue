<template>
  <div id="bill" class="bill">
    <div class="header">
      <h1>Safe Parking</h1>
    </div>
  </div>
  <div class ="main-component">
    <h2>Vehiculo</h2>
    <form class="form-container">
      <div class="form-group">
        <label for="placa">Placa</label>
        <input type="text" class="form-control" id="placa" placeholder="Placa" v-model="client.licensePlate">
      </div>
      <div class="form-group">
      <label for="horaEntrada">Entrada</label>
      <input type="datetime" class="form-control" id="horaEntrada" v-model="client.entryDate" placeholder="Fecha de ingreso">
      </div>
      <div class="form-group">
      <label for="horaSalida">Salida</label>
      <input type="datetime" class="form-control" id="horaSalida" v-model="client.exitdate" placeholder="Fecha de salida">
      </div>
      <div class="form-group">
      <label for="tiempo">Tiempo de Uso</label>
      <input type="text" class="form-control" id="tiempo" v-model="client.useTime" placeholder="Tiempo total">
      </div>
      <div class="form-group">
      <label for="costo">Costo</label>
      <input type="text" class="form-control" id="costo" v-model="client.cost" placeholder="Costo total">
      </div>
      <div class="button-group">
        <button v-on:click="clear">Cancelar</button>
        <button v-on:click="safe">Guardar</button>
      </div>
    </form>
  </div>
  <div class ="footer">
  </div>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      client: {
        placa: '',
        entryDate: '',
        exitdate: '',
        useTime: '',
        cost: ''
      }
    }
  },

  /* components: {
  }, */

  methods: {
    clear: function () {
      this.message = ''
    },
    safe: function () {
      this.$router.push({})
    }
  }

  /* created () {
    console.log('Component created!')
  } */

}
</script>
<style>

.form-group {
  margin-left: 15px;
  margin-right: 15px;
  margin-top: 15px;
  margin-bottom: 15px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.button-group {
  border-radius: 50px;
  margin-left: 15px;
  margin-right: 15px;
  margin-top: 15px;
  margin-bottom: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
