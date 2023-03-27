<script>
    export default {
        name: 'TheFooter'
    }
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="links">
                <div>
                    <ul>
                        <li class="title-list"><a href="#">titolo</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                    </ul>
                    <ul>
                        <li class="title-list"><a href="#">titolo</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li class="title-list"><a href="#">titolo</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li class="title-list"><a href="#">titolo</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                        <li><a href="#">link</a></li>
                    </ul>
                </div>
            </div>
            <div class="big-logo"></div>
        </div>
        
    </footer>
</template>

<style  lang="scss" scoped>
    @use '../styles/general.scss';

    .footer{
        height: 250px;
        background-image: url(../assets/footer-bg.jpg);

        .container {
        display: flex;
        justify-content: space-between;
        height: 100%;
        width: 1000px;
        margin: auto;
        }

        .links {
            width: 40%;
            height: 100%;
            padding: 10px;
            display: flex;
        

            div{
                height: 100%;
                width: calc(100% / 3);

                ul{
                    display: flex;
                    flex-direction: column;

                    li {
                        list-style: none;
                        font-size: 13px;
                    }

                    a {
                        text-decoration: none;
                        color: white;
                    }
                }
            }
        }
    }
    
    .title-list {
        padding: 10px 0;
        text-transform: uppercase;
        font-size: 18px;
    }
    .big-logo {
    width: 60%;
    height: 100%;
    text-align: center;
    background-image: url(/src/assets/dc-logo-bg.png);
    background-position-y: center;
    background-position-x: right;
    background-repeat: no-repeat;
    background-size: 400px;
}
</style>