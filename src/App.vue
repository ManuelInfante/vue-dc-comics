<template>
  <div>
    <Header />
    <Jumbotron url="jumbotron.jpg" />
    <MainSection />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import MainSection from './components/MainSection.vue';
import Footer from './components/Footer.vue';



export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    MainSection,
    Footer,
  }
}
</script>

<style lang="scss">
@import "@/style/generals";

</style>
