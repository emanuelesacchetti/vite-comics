<script>
    export default {
        name: 'TheBlackBanner',
        data(){
            return {
                social: [
                    {
                        pre: '../assets/',
                        name:'footer-pinterest.png'
                    },
                    {
                        pre: '../assets/',
                        name:'footer-facebook.png'
                    },
                    {
                        pre: '../assets/',
                        name:'footer-periscope.png'
                    },
                    {
                        pre: '../assets/',
                        name:'footer-twitter.png'
                    },
                    {
                        pre: '../assets/',
                        name:'footer-youtube.png'
                    }
                ]
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
                    <img :src='element.pre + element.name'>
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

    a {
    padding: 5px;
    margin: 0 10px;
    background-color: gray;
    width: 30px;
    height: 30px;
    border-radius: 50%;
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