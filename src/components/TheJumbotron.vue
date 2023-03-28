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
    .bg{
        height: 300px;
        width: 100%;
        background-image: url(../assets/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        

        .container {
            width: 1000px;
            margin: auto;
            height: 100%;
            position: relative;

            .absolute-btn {
            position: absolute;
            bottom: -20px;
            left: 50px;
            padding: 10px;
            background-color: #0282f9;
            color: white;
            }
        }

    }
</style>
