<script>
export default{
    name: 'TheJumbotron'
}

</script>


<template>
    <div class="bg">
        <div class="container">
            <span class="absolute-btn">CURRENT SERIES</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../styles/general.scss";
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins';

    .bg{
        height: 300px;
        width: 100%;
        background-image: url(../assets/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;

        .container {
            @include mixins.container;
            position: relative;
        }
        .absolute-btn {
            position: absolute;
            bottom: -20px;
            left: 50px;
            padding: 10px;
            background-color: $color-secondary;
            color: white;
        }
    }
</style>
