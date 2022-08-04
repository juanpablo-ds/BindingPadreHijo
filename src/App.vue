<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  
  <input type="text" v-model="texto"/>
  <button @click="setTexto()"> Enviar </button>
  
  <componente-hijo  :mensaje_recibido="texto_enviar" >    </componente-hijo> 
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ComponenteHijo from './componenteHijo/componenteHijo.vue';

export default {
  name: 'App',

  data: () => ({
    
      
      texto: "--",
      texto_enviar: "",
      contador: 1
  }),
  
  components: {
    
    ComponenteHijo
  },

  methods:{
    setTexto(){
        this.texto_enviar = this.texto
        // this.texto="aaaa: "+this.contador
        // this.contador++;
        
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
