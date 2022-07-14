<template>
  <div id="app">
    <div class="wrapper_switch" :style="textoDerecha">
      Modo Noche <img src="img/luna.svg" width="15px" height="15px">
      <label class="switch">
      <input type="checkbox" @click="cambiarVista()">
      <span class="slider round"></span>
      </label>
    </div>
    <miTabla
      :lista="elenco"
      :darkmode="darkmode"
    ></miTabla>
  </div>
</template>

<script>
import miTabla from './components/miTabla.vue'

export default {
  name: 'App',
  components: {
    miTabla
  },
  data(){
    return{
      elenco: [
                  {
                      id: 1,
                      nombre: 'Leonardo DiCaprio',
                      personaje: 'Rick Dalton'
                  },
                  {
                      id: 2,
                      nombre: 'Brad Pitt',
                      personaje: 'Cliff Booth'
                  },
                  {
                      id: 3,
                      nombre: 'Margot Robbie',
                      personaje: 'Sharon Tate'
                  },
                  {
                      id: 4,
                      nombre: 'Margaret Qualley',
                      personaje: '«Pussycat»'
                  }
          ],
          darkmode: false,
          textoDerecha: {'text-align' : 'right'}
    }
  },
  methods: {
        cambiarVista(){
            this.darkmode = !this.darkmode 
        }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
