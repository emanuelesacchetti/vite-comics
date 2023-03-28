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
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins';

.banner {
    background-color: $color-bg-dark;
    height: 70px;

    .container {
    @include mixins.container;
    @include mixins.d-flex(space-between);
}
}
.social {
    @include mixins.d-flex;

    img {
        margin: 0 10px;
    }
    .follow {
    color: $color-secondary;
    padding: 0 10px;
    text-transform: uppercase;
    font-weight: bold;
    }
}

button{
    color: white;
    border: 2px $color-secondary solid;
    padding: 10px;
    background-color: $color-bg-dark;
}

</style>