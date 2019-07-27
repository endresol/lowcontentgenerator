<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <SlideGenerator msg="Google Slides Generator"/>
  </div>
</template>

<script>
import SlideGenerator from './components/SlideGenerator.vue'

export default {
  name: 'app',
  components: {
    SlideGenerator
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
