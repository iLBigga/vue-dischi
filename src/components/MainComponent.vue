<template>
    <main class="main-section py-5">
        <div class="container">
            <div class="row row-cols-5 g-3">
                <div 
                    v-for="(album, i) in albumList"
                    :key="i"
                    class="col"
                >
                    <CardsComponent :item="album"/>
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
            albumList: [],
        }
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
                this.albumList = res.data.response;
                console.log(res.data.response)
            });    
    },
};
</script>


<style lang="scss" scoped>
    @import "../styles/variables";

    .main-section{
        background-color: $dark-blue;
        flex-grow: 1;
    }
</style>