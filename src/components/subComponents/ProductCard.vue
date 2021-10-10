<template>
    <div class="product-container">
        <div class="img-container">
            <img :src="data.thumb" :alt="data.series">
        </div>

        <h2 class="font-xs white-text text-uppercase">
            {{data.series}}
        </h2>
    </div>
</template>

<script>
export default {
    name: 'ProductCard',
    props:[
        'data',
    ],
}
</script>

<style scoped lang="scss">
@import "@/style/generals";

.product-container{
    width: 200px;
    padding-bottom: 40px;

    .img-container{
        height: 200px;
        width: 100%;

        img{
            height: 100%;
            width: 100%;
            object-fit: cover;
            object-position: top;
        }
    }
}
</style>