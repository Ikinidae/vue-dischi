<template>
  <div class="card">
    <img :src="albumObject.poster" :alt="albumObject.title">
    <h2>{{albumObject.title}}</h2>
    <p>{{albumObject.author}}</p>
    <p>{{albumObject.year}}</p>
  </div>
</template>

<script>
export default {
  name: 'MusicCard',
  props: {
      albumObject: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
