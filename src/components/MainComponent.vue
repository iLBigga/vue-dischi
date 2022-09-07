<template>
    <main class="main-section">
        <div class="container">
            <div class="row">
                <div 
                    v-for="(album, i) in albumList"
                    :key="i"
                >
                    <CardsComponent/>
                </div>
            </div>
        </div>        
    </main>
</template>


<script>
    import axios from "axios";
    import CardsComponent from './CardsComponent.vue';

export default {
    name: "MainComponent",
    components: {
        CardsComponent,
    },
    data(){
        return {
            albumList: []
        }
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
                this.albumList = res.data;
            });    
    },
};
</script>


<style lang="scss" scoped>
    @import "../styles/variables";

    .main-section{
        background-color: $dark-blue;
        height: 100vh;
        widows: 100vw;
    }
    
</style>