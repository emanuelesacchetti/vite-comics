<script>
    export default {
        name: 'TheFooter',
        data(){
            return {
                comics: [
                    'Characters',
                    'Comics','Movie',
                    'TV','Games',
                    'Videos','News'
                ],
                shop: ['Shop DC','Shop DC Collectibles'],
                dc: ['Terms Of Use',
                    'Privacy policy(new)',
                    'Ad choices',
                    'Advertising',
                    'jobs','Subscriptions',
                    'Talent Workshops',
                    'Rating','Shop Help',
                    'Contact us'
                    ],
                sites: ['DC','MAD magazine',
                        'DC Kids','DC Universe',
                        'DC Power Visa'
                    ]
            }
        }
    }
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="links">
                <div>
                    <ul>
                        <div class="title-list">DC COMICS</div>
                        <li v-for="link in comics">
                            <a href="#">{{ link }}</a>
                        </li>
                    </ul>
                    <ul>
                        <div class="title-list">SHOP</div>
                        <li v-for="link in shop">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <div class="title-list">DC</div>
                        <li v-for="link in dc">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <div class="title-list">SITES</div>
                        <li v-for="link in sites">
                            <a href="#">{{link}}</a>
                        </li>
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
                        color: gray;
                        font-size: 10px;
                    }
                }
            }
        }
    }
    
    .title-list {
        padding: 10px 0;
        font-size: 12px;
        font-weight: bold;
        color: white;
        text-transform: uppercase;
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