<template>
  <section>
    <h1 v-on:click="loadData">{{ msg }} - {{category}} - {{type}}</h1>
<!--
    <div v-for="(value, key) in info">
      {{ key }} : {{ value }}
    </div> -->
    <ul>
      <li><strong>ID:</strong> {{info.id}}</li>
      <li><strong>Title:</strong> {{info.title}}</li>
      <li><strong>Body:</strong> {{info.body}}</li>
    </ul>

  </section>
</template>

<script>
  const apiURL = 'https://jsonplaceholder.typicode.com/posts/1'

  export default {
    name: 'test',
    data () {
      return {
        msg: 'Testing...',
        info: {}
      }
    },
    props: [
      'type',
      'category'
    ],
    mounted () {
      this.loadData()
    },
    methods: {
      loadData: function () {
        this.$http.get(apiURL).then((response) => {
          // success callback
          this.info = response.body

          console.log(response)
        }, (response) => {
          // error callback
        })
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
  padding: 1em;
  text-align: left;
}

li {
  display: block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>