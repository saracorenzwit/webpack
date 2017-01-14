<template>
  <div id="app">
    <homepage></homepage>
    <concerns category="in-person" type="climate"></concerns>
    <concerns category="donate" type='healthcare'></concerns>
  </div>
</template>

<script>
import Homepage from './components/Homepage'
import Concerns from './components/Concerns'

export default {
  name: 'app',
  components: {
    Homepage,
    Concerns
  },
  mounted () {
    console.log('Good Morning, How Do I Help?')
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
