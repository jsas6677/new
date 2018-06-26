<template>
  <div class="hello">
     <h1>{{ msg }}</h1>
     <h2>Let's see</h2>
    <ul>
      <button href="#" type="button" class="btn success" style="position: relative;"><div class="btn__content">Next</div></button>
    </ul>
  <vue-particles
      color= "#7B1FA2"
      :particleOpacity="0.9"
      :particlesNumber= "120"
      shapeType="polygon"
      :particleSize="6"
      linesColor="#00acd6"
      :linesWidth="1"
      :lineLinked="true"
      :lineOpacity="0.4"
      :linesDistance="100"
      :moveSpeed="6"
      :hoverEffect="true"
      hoverMode="grab"
      :clickEffect="true"
      clickMode="repulse">
      </vue-particles>
    </div>
</template>

<script>
import Vue from 'vue'
import VueParticles from 'vue-particles'
Vue.use(VueParticles)
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to vue'
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
