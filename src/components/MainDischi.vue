<template>
    <main>
        <SearchGenre @search="changeSelectedGenre"/>

        <div id="card_container">
            <MusicCard v-for="(item, i) in filteredAlbum" :key="i" :albumObject="item" />
        </div>
    </main>
</template>

<script>
import MusicCard from './MusicCard.vue'
import axios from "axios"
import SearchGenre from "./SearchGenre.vue"

export default {
    name: "MainDischi",
    components: {
        MusicCard, SearchGenre
    },
    data() {
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albumList: [],
            selectGenre: "all"
        }
    },
    created() {
        this.getAlbum();
    },
    methods: {
        getAlbum() {
            axios
                .get(this.apiUrl)
                .then((result) => {
                    this.albumList = result.data.response;
                })
                .catch((error) => {
                    console.log("Errore", error);
                })
        },
        changeSelectedGenre(key) {
            this.selectGenre=key;
        }
    },
    computed: {
        filteredAlbum() {
            if (this.selectGenre === "all") {
                return this.albumList;
            } else {
                return this.albumList.filter(item => {
                    return item.genre.toLowerCase().includes(this.selectGenre);
                })
            }
        }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main {
    background-color: #1e2d3b;
    padding: 30px 200px;
    height: calc(100vh - 50px);

    #card_container {
        display: flex;
        flex-wrap: wrap;
        height: calc(100vh - 100px);
        overflow: auto;
    }
}
</style>