<template>
    <header class="p-4 d-flex justify-content-between">
        <img class="logo_spotify" src="../assets/Spotify_logo_without_text.svg.png" alt="">
        <select 
            v-model="genere" 
            @click="$emit('findGenre', genere)" 
            class="align-self-center select" 
            name="genre" 
            id="genre">

                <option v-for="(genre, i) in options" :key="i">{{genre}}</option>

        </select>
    </header>
</template>


<script>
export default {
    name: "HeaderComponent",
    data() {
        return {
            genere: '',
            options: [
                '',
                'Rock',
                'Pop',
                'Jazz',
                'Metal',
            ],
        };
    },
};
</script>


<style lang="scss" scoped>

    @import "../styles/variables";
    @import "../styles/general.scss";

    header{
        background-color: $light-blue;

        .logo_spotify {
            width: 50px;
        }

        .select {
            padding: 0 1rem;
        }
    }
</style>