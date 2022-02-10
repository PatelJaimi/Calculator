<template>
  <div id="app">
    <Cal />
  </div>
</template>

<script>
import Cal from './components/Cal.vue'

export default {
  name: 'App',
  components: {
    Cal
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
