<script>
    export default {
        name: 'TheFooter'
    }
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="links">ciao</div>
            <div class="big-logo"></div>
        </div>
        
    </footer>
</template>

<style  lang="scss">
    .footer{
        height: 250px;
        background-image: url(../assets/footer-bg.jpg);
    }
    .container {
        display: flex;
        justify-content: space-between;
        height: 100%;

    }
    .links {
        width: 40%;
        height: 100%;
    }
    .big-logo {
    width: 60%;
    height: 100%;
    text-align: center;
    background-image: url(/src/assets/dc-logo-bg.png);
    background-position-y: center;
    background-repeat: no-repeat;
    background-size: 400px;
}
</style>