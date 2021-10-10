<template>
  <div class="jumbo">
      <img :src="require('@/assets/img/' + url)" alt="">
  </div>
</template>

<script>
export default {
    name:'Jumbotron',
    props:[
        'url',
    ]
}
</script>

<style scoped lang="scss">

.jumbo{
    height: 50vh;

    img{
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>