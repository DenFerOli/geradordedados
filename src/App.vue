<template>
  <div id="app">
    <CPFComponent />
  </div>
</template>

<script>
import CPFComponent from './components/CPFComponent.vue'


export default {
  name: 'App',
  components: {
    CPFComponent

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
