<template>
  <div id="app">
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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
