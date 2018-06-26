<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div @click="getData()">
    Get Data
    </div>
    <h2>Essential Links</h2>
    <ul>
      <input
      type="button"
      href=""
      target="_blank"
      value="Refresh"
      />
      <input
      type="button"
      href="/"
      target="_blank"
      value="Back"
      />
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default{
  data () {
    return {
      post: [],
      msg: ''
    }
  },
  mounted () {
  },
  methods: {
    getData () {
      // this.$http.get('https://api.chucknorris.io/jokes/random').then(function (value) {
      //   console.log(value)
      // })
      axios.get('https://api.chucknorris.io/jokes/random').then(value => {
        this.post = value
        console.log(value)
        this.msg = value.data.value
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
