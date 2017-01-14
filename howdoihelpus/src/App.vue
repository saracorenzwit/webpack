<template>
  <div id="app">
    <homepage></homepage>
  </div>
</template>

<script>
import Homepage from './components/Homepage'

export default {
  name: 'app',
  components: {
    Homepage
  }
}
</script>

<style>
#app {
  font-family: 'Work Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
