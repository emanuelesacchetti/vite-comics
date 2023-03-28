<script>
    export default {
        name: 'TheBlackBanner',
        data(){
            return {
                social: [
                'footer-pinterest.png',
                'footer-facebook.png',
                'footer-periscope.png',
                'footer-twitter.png',
                'footer-youtube.png'
                ]
            };
        },
        methods: {
            getImagePat: function(img){
            return new URL(`../assets/${img}`, import.meta.url) .href;
        }
    }
}
</script>

<template>
    <div class="banner">
        <div class="container flex">
            <button>SIGN-UP NOW</button>
            <div class="social flex">
                <div class="follow">follow us</div>
                <a href="#" v-for="element in social">
                    <img :src=getImagePat(element)>
                </a>
            </div>
        </div>
    </div>
</template>

<style  lang="scss" scoped>
@use '../styles/general.scss';

.banner {
    background-color: #303030;
    height: 70px;

    .container {
    width: 1000px;
    margin: auto;
    height: 100%;
}
}

.container.flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.social.flex {
    display: flex;
    align-items: center;
    justify-content: center;

    img {
        margin: 0 10px;
    }

    .follow {
    color: #0282f9;
    padding: 0 10px;
    text-transform: uppercase;
    font-weight: bold;
    }
}

button{
    color: white;
    border: 2px #0282f9 solid;
    padding: 10px;
    background-color: #303030;
}

</style>