<template>
    <div class="custom_card">
        <img :src="item.poster">
        <div class="card_body">
            <p class="card_title">{{item.title}}</p>
            <p class="card_author">{{item.author}}</p>
            <p class="card_year">{{item.year}}</p>
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

            .card_title {
                font-size: 1.3rem;
                text-transform: uppercase;
            }

            .card_author, .card_year{
                color: lightslategray;
                margin: 0;
            }
    }

</style>