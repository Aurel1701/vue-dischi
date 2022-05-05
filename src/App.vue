<template>
  <div id="app">
    <HeaderAlt/>
  </div>
</template>

<script>
import HeaderAlt  from './components/HeaderAlt.vue'

export default {
  name: 'App',
  components: {
    HeaderAlt, 
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
