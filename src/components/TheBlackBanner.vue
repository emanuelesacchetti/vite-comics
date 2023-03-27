<script>
    export default {
        name: 'TheBlackBanner'
    }
</script>

<template>
    <div class="banner">
        <div class="container flex">
            <button>SIGN-UP NOW</button>
            <div class="social flex">
                <div class="follow">follow us</div>
                <a href="#"></a>
                <a href="#"></a>
                <a href="#"></a>
                <a href="#"></a>
                <a href="#"></a>
            </div>
        </div>
    </div>
</template>

<style  lang="scss" scoped>
@use '../styles/general.scss';

.banner {
    background-color: black;
    height: 70px;
}
.container {
    width: 1000px;
    margin: auto;
    height: 100%;
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
}
.social a {
    padding: 5px;
    margin: 0 10px;
    background-color: gray;
    width: 30px;
    height: 30px;
    border-radius: 50%;
}
.follow {
    color: blue;
    padding: 0 10px;
    text-transform: uppercase;
}
button{
    color: white;
    border: 2px blue solid;
    padding: 10px;
    background-color: black;
}

</style>