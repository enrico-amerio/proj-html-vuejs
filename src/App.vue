<script>
import Nav from './components/Nav.vue';
import Jumbo from './components/Jumbo.vue';
import Main from './components/Main.vue';
  export default {
    components:{
      Nav,
      Jumbo,
      Main
    }
  }
</script>

<template>
  <Nav/>
  <Jumbo />
  <Main />
</template>



<style lang="scss" scoped>
@use './assets/scss/main.scss';
</style>