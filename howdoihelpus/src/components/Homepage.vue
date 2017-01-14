<template>
  <section>
    <h1>{{ msg }}</h1>
    <section class="issues">
      <ul>
        <li><a>Climate Change</a></li>
        <li><a>Education</a></li>
        <li><a>Equality</a></li>
        <li><a>Economy</a></li>
        <li><a>Foreign Policy</a></li>
        <li><a>Healthcare</a></li>
      </ul>
    </section>
  </section>
</template>

<script>
  export default {
    name: 'homepage',
    data () {
      return {
        msg: 'I wanna help!'
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>