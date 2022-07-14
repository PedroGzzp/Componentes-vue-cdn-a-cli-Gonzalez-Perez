<template>
  <table :class="{'table table-striped table-bordered' : !darkmode, 'table table-striped table-bordered table-dark' : darkmode}">
            <thead>
                <tr>
                    <th colspan="2" class="text-center">Elenco</th>
                </tr>
                <tr>
                    <th>Actor/Actriz</th>
                    <th>Personaje</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="items in lista" :key="items.id">
                    <td>{{items.nombre}}</td>
                    <td>{{items.personaje}}</td>
                </tr>
            </tbody>
  </table>
</template>

<script>
export default {
  name: 'miTabla',
  props: {
    lista: Array,
    darkmode: Boolean
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
