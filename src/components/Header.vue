<template>
  <div class=" container flex justify-spaceBetween">
    <div class="logo">
      <a href="/" class="flex align-center">
        <img src="@/assets/img/dc-logo.png" alt="">
      </a>
    </div>

    <nav>
      <ul class="flex">
        <li v-for="(link, index) in links" :key="index">
          <a :href="link.url" :class="(link.current) ? 'active' : null" class="text-center font-min">
            {{link.text.toUpperCase()}}
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
import {headerLinks} from "@/data/Links.js"

export default {
  name: 'Header',
  data(){
    return{
      links: headerLinks,
    }
  }
}
</script>

<style scoped lang="scss">
@import "@/style/generals";

.container{
  height: 80px;

  .logo{
    height: 100%;

    a{
      height: 100%;
      transition: all 0.3s;

      img{
        height: 75%;
      }

      &:hover{
        transform: scale(0.8);
      }
    }
  }

  nav{
    height: 100%;

    ul{
      height: 100%;

      li{
        min-width: 90px;
        height: 100%;
      }

      a, a:visited{
        color: $black;
        line-height: calc(80px - 4px);
        border-bottom: 4px solid transparent;
        display: inline-block;
        height: 100%;
        width: 100%;

        &.active{
          color: $primary;
          border-color: $primary;
        }
      }
    }
  }
}
</style>
