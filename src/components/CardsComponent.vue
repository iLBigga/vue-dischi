<template>
    <div class="custom_card">
        <img :src="item.poster">
        <div class="card_body py-3">
            <p class="title">{{item.title}}</p>
            <div class="card_author">
                <p class="author">{{item.author}}</p>
                <p class="year">{{item.year}}</p>
          </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "CardsComponent",
    props: {
        item: Object,
    },
}
</script>


<style lang="scss" scoped>

    @import "../styles/general.scss";
    @import "../styles/variables.scss";

    .custom_card{
        color: white;
        padding: 1rem;
        height: 100%;
        background-color: $light-blue;
        text-align: center;

            .title {
                font-size: 1.3rem;
                font-weight: bold;
                text-transform: uppercase;
            };


            .card_author {
                font-size: 1.2rem;

                .author, .year{
                color: lightslategray;
                margin: 0;
                };
            };        
    };
</style>