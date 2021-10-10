<template>
    <main>
        <div class="background">
            <div class="container">
                <div class="card-container font-xxl flex justify-spaceBetween wrap">
                    <ProductCard 
                    v-for="(product, index) in products" :key="index"
                    :data="product"
                    />
                </div>

                <span class="title-box font-sm white-text text-uppercase">
                    current series
                </span>

                <div class="button-container text-center">
                    <a href="#" class="white-text text-uppercase">
                        load more
                    </a>
                </div>
            </div>
        </div>
        <div>
            <MainBanner />
        </div>
    </main>
</template>

<script>
import dataProducts from "@/data/dc-comics.json";
import ProductCard from "@/components/subComponents/ProductCard.vue";
import MainBanner from "@/components/subComponents/MainBanner.vue";

export default {
    name: 'MainSection',
    components: {
        ProductCard,
        MainBanner,
    },
    data(){
        return{
            products: dataProducts,
        }
    }
}
</script>

<style scoped lang="scss">
@import "@/style/generals";

.background{
    background-color: $gray;

    .container{
        position: relative;
        padding-top: 50px;

        .title-box{
            position: absolute;
            left: 0;
            top: 0;
            transform: translate(0, -50%);
            background-color: $primary;
            padding: 10px 15px;
            font-weight: 800;
        }

        .button-container{
            padding-bottom: 30px;

            a{
                background-color: $primary;
                padding: 10px 60px;
                font-weight: 800;
            }
        }
    }
}
</style>