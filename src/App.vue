<template>
  <div id="app">
    <NavBar />
    <AppMovies />  
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'
import AppMovies from './components/AppMovies.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    NavBar,
    AppMovies
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
