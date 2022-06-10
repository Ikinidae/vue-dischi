<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <HeaderDischi/>
    <MainDischi/>
  </div>
</template>

<script>
import HeaderDischi from './components/HeaderDischi.vue'
import MainDischi from './components/MainDischi.vue'

export default {
  name: 'App',
  components: {
    HeaderDischi,
    MainDischi
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
