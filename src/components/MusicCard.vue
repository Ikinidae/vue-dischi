<template>
  <div class="card">
    <img :src="albumObject.poster" :alt="albumObject.title">
    <h3>{{albumObject.title}}</h3>
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
    .card {
        width: 18%;
        background-color: #2e3a46;
        margin: 10px;
        padding: 15px 10px;
        text-align: center;
        height: 300px;

        img {
            width: 150px;
            height: 150px;
            object-fit: cover;
        }

        h3 {
            color: white;
            text-transform: uppercase;
        }

        p {
            color: gray;
        }
    }
</style>
