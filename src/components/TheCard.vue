<script>
export default{
    name: 'TheCard',
    props:{
        image: 'string',
        text: 'string'
    }
}

</script>


<template>
    <div class="card">
        <div class="img-wrapper">
            <img :src="image" :alt="text">
        </div>
        <h4>{{ text }}</h4>
    </div>
</template>


<style lang="scss" scoped>

.img-wrapper {
    width: 100%;
    height: 5%;
}        
img{
    height: 200px;
    width: 100%;
}
h4 {
    color: white;
    font-size: 13px;
}
    
</style>