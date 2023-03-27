<script>
    export default {
        name: 'TheHeader',
        data(){
            return{
                links: [
                    'characters',
                    'comics',
                    'movie',
                    'tv',
                    'games',
                    'collectibles',
                    'videos',
                    'fans',
                    'news',
                    'shop'
                ]
            }
        }
    }

</script>

<template>
    <header>
        <div class="container flex-center-between">
            <img src="../assets/dc-logo.png" alt="logo DC">
            <nav>
                <ul>
                    <li v-for="(link, index) in links">
                        <a href="#">{{ link }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style  lang="scss" scoped>
    @use '../styles/general.scss';
    @use '../styles/partials/mixins';
    
    header {
        background-color: white;
        height: 70px;

        .container{
        width: 1000px;
        margin: auto;
        height: 70px;
        }
        .flex-center-between {
        display: flex;
        align-items: center;
        justify-content: space-between;
        }
    }
    
    
    img{
        height: 50px;
    }
    nav {
        height: 100%;

        ul {
        display: flex;
        align-items: center;
        list-style: none;
        height: 100%;
        margin: 0;

            li {
            padding: 0 10px;
            height: 100%;
            display: flex;
            align-items: center;
            border-bottom: 3px solid antiquewhite;

                &:hover {
                border-bottom: 3px solid blue;
                }

                    &:hover a {
                        color: blue;
                    }

                a {
                text-decoration: none;
                color: black;
                text-transform: uppercase;
                font-size: 12px;
                }
            }
        }

    }
    
    
     
    
    
</style>