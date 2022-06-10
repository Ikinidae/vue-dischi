<template>
    <header>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
    </header>
</template>

<script>
export default {
  name: 'HeaderDischi',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    header {
        height: 50px;
        background-color: #2e3a46;

        img {
            width: 40px;
            padding-left: 10px;
            padding-top: 9px;
        }
    }
</style>
