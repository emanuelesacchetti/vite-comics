<script>
    export default {
        name: 'TheBlueBanner',
        data(){
            return {
                buy: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        text: 'DIGITAL COMICS'
                    },
                    {
                        img: 'buy-comics-merchandise.png',
                        text: 'MERCHANDISE'
                    },
                    {
                        img:  'buy-comics-shop-locator.png',
                        text: 'SHOP LOCATOR'
                    },
                    {
                        img:  'buy-comics-subscriptions.png',
                        text: 'SUBCRIPTIONS'
                    }
                ]
            }
        },
        methods: {
            getImagePat: function(img){
            return new URL(`../assets/${img}`, import.meta.url) .href;
        }
    }
    }
</script>

<template>
    <div class="blue-banner">
        <div class="container flex">
            <div class="item flex" v-for="element in buy">
                <img :src=getImagePat(element.img)>
                <div class="text">{{ element.text }}</div>
            </div>
        </div>
    </div>
</template>

<style  lang="scss" scoped>
    @use '../styles/general.scss';
    

    .blue-banner{
        height: 130px;
        background-color: #0282f9;
        color: white;

        .container{
        width: 1000px;
        margin: auto;
        height: 100%;
        }

        .item{
            height: 50px;
            margin: 0 20px;

            img{
                height: 100%;
            }
            .text{
                margin: 0 10px;
            }
        }
    }
    .flex{
        display: flex;
        justify-content: center;
        align-items: center;
    }

</style>