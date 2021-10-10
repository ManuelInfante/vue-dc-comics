<template>
    <div>
        <div id="footerTop">
            <div class="container flex justify-spaceBetween">
                <ul class="links-container flex column wrap">
                    <li v-for="(linksContainer, index) in linksContainers" :key="index">
                        <h3 class="font-s white-text">
                            {{linksContainer.category.toUpperCase()}}
                        </h3>

                        <ul>
                            <li v-for="(link, index) in linksContainer.links" :key="index">
                                <a :href="link.url" class="font-xxs text-capitalize">
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>

        <div id="footerBottom">
            <div class="container flex justify-spaceBetween align-center">
                <a href="#" class="text-uppercase font-s white-text">
                    sign-up now!
                </a>

                <div class="social-container flex align-center">
                    <a href="#" class="font-s text-uppercase">
                        follow us
                    </a>

                    <div>
                        <a href="#"><img src="@/assets/img/footer-facebook.png" alt="facebook"></a>
                        <a href="#"><img src="@/assets/img/footer-periscope.png" alt="periscope"></a>
                        <a href="#"><img src="@/assets/img/footer-pinterest.png" alt="pintrest"></a>
                        <a href="#"><img src="@/assets/img/footer-twitter.png" alt="twitter"></a>
                        <a href="#"><img src="@/assets/img/footer-youtube.png" alt="youtube"></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import {footerLinks} from "@/data/Links.js"

export default {
    name:'Footer',
    data(){
        return{
            linksContainers: footerLinks,
        }
    }
}
</script>

<style scoped lang="scss">
@import "@/style/generals";

#footerTop{
    background-image: url('~@/assets/img/footer-bg.jpg');
    height: 40vh;

    .container{
        height: 100%;
        padding: 40px 0;
        background-image: url('~@/assets/img/dc-logo-bg.png');
        background-position: right center;
        background-repeat: no-repeat;

        .links-container{
            height: 100%;

            & > li{
                margin-right: 25px;

                & > ul{
                margin: 20px 0;
                }

                & a{
                    color: rgb(170, 170, 170);
                    line-height: 5px;
                }
            }
        }
    }
}

#footerBottom{
    background-color: $lightgray;

    .container{
        padding: 30px 0;

        & > a{
            display: block;
            padding: 10px;
            border: 2px solid $primary;
        }

        & .social-container{

            & > a{
                color: $primary;
                margin-right: 15px;
            }

            & img{
                margin: 0 7px;
            }
        }
    }
}
</style>