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
        <div class="cont">
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
    @use '../styles/partials/variables' as *;
    
    header {
        background-color: white;
        height: 70px;

        .cont{
            @include mixins.container;
            @include mixins.d-flex(space-between);
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
            @include mixins.d-flex;
            border-bottom: 3px solid antiquewhite;

                &:hover {
                border-bottom: 3px solid $color-secondary;
                }
                    &:hover a {
                        color: $color-secondary;
                    }
                a {
                text-decoration: none;
                color: $color-bg-dark;
                text-transform: uppercase;
                font-size: 12px;
                }
            }
        }

    }
    
    
     
    
    
</style>