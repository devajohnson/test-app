<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Getelement />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Getelement from './components/Getelement.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld
    Getelement
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
