<script>
import EventCard from './partials/EventCard.vue'
export default {
  components:{
    EventCard
  }
}
</script>

<template>
  <div class="wrapper">
    <img src="../assets/img/h1-img-09.jpg" alt="">
    <div class="container">
      <EventCard/>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.wrapper{
  position: relative;
    width: 100%;
    z-index: -1;
    display: flex;
    flex-direction: column;
  img{
    img{
      width: 100%;
      height: 90vh;
      max-height: 1000px;
          object-fit: cover;
    }
  }
}
</style>