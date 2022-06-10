<template>
  <div>
    <MusicCard
        v-for="(item, i) in albumList"
        :key="i"
        :albumObject="item"
    />
  </div>
</template>

<script>
import MusicCard from './MusicCard.vue'
import axios from "axios"

export default {
    name: "MainDischi",
    components: {
        MusicCard
    },
    data () {
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albumList: []
        }
    },
    created () {
        this.getAlbum();
    },
    methods: {
        getAlbum () {
            axios
            .get(this.apiUrl)
            .then((result) =>{
                this.albumList = result.data.response;
                console.log(result);
            })
            .catch((error) => {
                console.log("Errore", error);
            })
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>