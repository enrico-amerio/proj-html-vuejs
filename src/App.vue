<script>
import Nav from './components/Nav.vue';
import Jumbo from './components/Jumbo.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import ScrollUp from './components/partials/ScrollUp.vue';
  export default {
    components:{
      Nav,
      Jumbo,
      Main,
      Footer,
      ScrollUp
    }
  }
</script>

<template>
  <Nav/>
  <ScrollUp/>
  <Jumbo />
  <Main />
  <Footer/>
</template>



<style lang="scss">
@use './assets/scss/main.scss';
</style>