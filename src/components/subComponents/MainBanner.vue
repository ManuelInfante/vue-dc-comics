<template>
    <div class="background-container">
        <div class="container">
            <ul class="flex align-center justify-spaceAround">
                <li v-for="(data, index) in database" :key="index">
                    <a :href="data.url" class="flex align-center">
                        <img :src="require('@/assets/img/' + data.img)" :alt="data.text">
                        <span class="font-xxs white-text">
                            {{data.text.toUpperCase()}}
                        </span>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MainBanner',
    data() {
        return{
            database: [
                {
                    img: 'buy-comics-digital-comics.png',
                    text: 'digital comics',
                    url: '#'
                },
                {
                    img: 'buy-comics-merchandise.png',
                    text: 'dc merchandise',
                    url: '#'
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    text: 'subscriptions',
                    url: '#'
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    text: 'comic shop locator',
                    url: '#'
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    text: 'dc power visa',
                    url: '#'
                },
            ],
        };
    },
}
</script>

<style scoped lang="scss">
@import "@/style/generals";

.background-container{
    background-color: $primary;

    .container{
        padding: 35px 0;
        
        li{
            a{
                img{
                    margin-right: 20px;
                }

                img:not([alt="comic shop locator"]){
                    width: 45px;
                }

                img[alt="comic shop locator"]{
                    height: 48px;
                }
            }
        }
    }
}

</style>