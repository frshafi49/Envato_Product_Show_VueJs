<template>
  <div id="app">
    <random-items/>
  </div>
</template>

<script>

import RandomItems from './components/RandomItems.vue'

export default {
  name: 'app',
  components: {
    RandomItems
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
