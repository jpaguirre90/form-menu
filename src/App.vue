<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <FormMenu/>
  </div>
</template>

<script>
import FormMenu from './components/FormMenu.vue'

export default {
  name: 'App',
  components: {
    FormMenu
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
