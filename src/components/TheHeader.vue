<script>
    export default {
        name: 'TheHeader'
    }
</script>

<template>
    <header>
        <div class="container flex-center-between">
            <img src="../assets/dc-logo.png" alt="logo DC">
            <nav>
                <ul>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                    <li><a href="">link</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style  lang="scss">
    @use '../styles/partials/mixins';
    body {
        padding:0;
        margin: 0;
        box-sizing: border-box;
    }
    header {
        background-color: antiquewhite;
        height: 70px;
    }
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
    img{
        height: 50px;
    }
    nav {
        height: 100%;
    }
    nav ul {
        display: flex;
        align-items: center;
        list-style: none;
        height: 100%;
        margin: 0;
    }
    ul li {
        padding: 0 10px;
        height: 97%;
        display: flex;
        align-items: center;
        border-bottom: 3px solid antiquewhite;
    }
    ul li:hover {
        border-bottom: 3px solid blue;
    } li:hover a {
        color: blue;
    }
    li a {
        text-decoration: none;
        color: black;
    }
</style>