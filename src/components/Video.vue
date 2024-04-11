<script>
import {store} from '../data/store'
import data from "../assets/db.json"

export default {
  data(){
      return{
        store,
        data
      }
    },
  }
</script>

<template>
  <div class="wrapper d-flex justify-content-center  align-items-center ">
    <div class="icon">
      <i class="fa-solid fa-play"></i>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  background-image:url('../assets/img/h1-img-04.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 900px;
  
  .icon{
    color:white;
    font-size: 50px;
    text-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

  }
}
</style>