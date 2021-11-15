<template>

 <!-- <prucess /> -->
<!-- <dynamic /> -->
 <!-- <div id="app container"> 
    <Projectbc class="row justify-content-left mt-3" :crumbs="crumbs" @selected="selected" />
  </div>  -->
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <Getelement /> -->
  <!-- <Hooks /> -->
  <!-- <Composite /> -->
  <Postelement />
</template>

<script>
// import dynamic from './components/dynamic.vue'
// import prucess from './components/prucess.vue'
// import Projectbc from './components/Projectbc.vue'
// import HelloWorld from './components/HelloWorld.vue'
// import Getelement from './components/Getelement.vue'
// import Hooks from './components/Hooks.vue'
// import Composite from'./components/Composite.vue'
import Postelement from'./components/Postelement.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld
    // Getelement,
    // Hooks,
    // Composite,
    Postelement,
    // Projectbc,
    // prucess,
    // dynamic
  },
  data(){
    return{
      crumbs: ['']
    }
  },
   methods: {
    selected(crumb) {
      console.log(crumb);
    }
   }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
