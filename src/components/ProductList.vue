<script>
    import TheCard from './TheCard.vue';

    export default{
        name: 'ProductList',
        components: {
        TheCard
        },
        data(){
            return {
                comics: [
                        {
                            "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$19.99",
                            "series": "Action Comics",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                            "price": "$3.99",
                            "series": "American Vampire 1976",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                            "price": "$16.99",
                            "series": "Aquaman",
                            "type": "graphic novel"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$2.99",
                            "series": "Batgirl",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640", 
                            "price": "$3.99",
                            "series": "Batman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                            "price": "$2.99",
                            "series": "Batman Beyond",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                            "price": "$3.99",
                            "series": "Batman/Superman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                            "price": "$4.99",
                            "series": "Batman/Superman Annual",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                            "price": "$5.99",
                            "series": "Batman: The Joker War Zone",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                            "price": "$6.99",
                            "series": "Batman: Three Jokers",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$4.99",
                            "series": "Batman: White Knight Presents: Harley Quinn",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$16.99",
                            "series": "Catwoman",
                            "type": "graphic novel"
                        }
                ]
            }
        }
    }

</script>


<template>
    <div>
        <div class="container flex">
            
            <div v-for="(comic,index) in comics" :key="index" class="box">
                <TheCard :image="comic.thumb" :text="comic.series"></TheCard>
            </div>

        </div>
        <div class="btn-wrap">
            <button class="btn"><a href="#">LOAD MORE</a></button>
        </div>

    </div>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins';
    .container {
        @include mixins.container;
        @include mixins.d-flex;
        padding: 50px 0;
    }
    .box{
        width: calc(100% / 6);
        padding: 10px;
        height: 280px;
    }
    .btn-wrap {
        @include mixins.d-flex;
    }
    .btn{
        padding: 10px 60px;
        background-color: $color-secondary;
        border: none;
        margin: 20px auto;

        a{
            text-decoration: none;
            color: white;
        }
    }

</style>