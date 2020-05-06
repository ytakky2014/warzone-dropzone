<template>
  <div id="app">
    <WarZone/>
  </div>
</template>

<script>
import WarZone from './components/WarZone'
export default {
  name: 'App',
  components: {
    WarZone
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
}
</style>