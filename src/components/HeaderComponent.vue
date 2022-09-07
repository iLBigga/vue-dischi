<template>
    <header class="p-4">
        <img class="logo_spotify" src="../assets/Spotify_logo_without_text.svg.png" alt="">
    </header>
</template>


<script>
export default {
    name: "HeaderComponent"
    
}
</script>


<style lang="scss" scoped>

    @import "../styles/variables";
    @import "../styles/general.scss";

    header{
        background-color: $light-blue;

        .logo_spotify {
            width: 50px;
        }
    }
</style>