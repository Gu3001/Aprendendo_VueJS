
<template>
  

  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Teste aplicação VUE, contador de likes"/>
  <h2 v-if="likes > 0 && likes < 10">
    Esse post teve {{likes}} 👍😁
  </h2>
  <h2 v-else-if="likes >= 10">
    Esse post teve {{likes}} 👍 Parabéns!!! 🥳
  </h2>
  <h2 v-else >
    Nenhum Like até agora! 😥
  </h2>

  <button v-on:click="aumentarLikes()" class="botaoLike" >Curtir</button>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
   data() {
      return {
        likes: 0
    }    
},
methods: {
      aumentarLikes(){
        this.likes++;
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
.botaoLike {
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
