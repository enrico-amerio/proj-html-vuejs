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
    methods:{
      getPathImage(img){
        return new URL(`../assets/img/${img}`, import.meta.url).href
      },
      goNext(){
        if(this.store.staffCounter < this.data.staff.length){
          this.store.staffCounter++
        }else{
          this.store.staffCounter = 1
        }
      },
      goPrev(){
        if(this.store.staffCounter > 1){
          this.store.staffCounter--
        }else{
          this.store.staffCounter = this.data.staff.length
        }
      }
    }
}
</script>

<template>
  <div class="container">
    <div class="data-wrapper" v-for="employee in data.staff" :key="employee.id">
      <div class="main-wrapper d-flex flex-wrap align-items-center justify-content-center" v-if="this.store.staffCounter == employee.id">
        <div class="img-wrapper" style="position: relative;">
          <img :src="getPathImage(employee.img)" alt="jumboImg">
          <div class="nav-arrows d-flex">
            <a @click="goPrev" class="my_btn full"><i class="fa-solid fa-arrow-left"></i></a>
            <a @click="goNext" class="my_btn full"><i class="fa-solid fa-arrow-right"></i></a>
          </div>
        </div>
        <div class="description-wrapper">
          <h3>{{ employee.name }}</h3>
          <p>{{ employee.role }}</p>
          <div class="line"></div>
          <p>{{ employee.description }}</p>
          <div class="icon-wrap">
            <a href="#" class="social-icon"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-twitter"></i></a>
          </div>
        </div>
        <img class="pattern" src="../assets/svg/svg-4.svg" alt="pattern">
      </div>
    </div>
  </div>
</template>



<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as * ;
@use '../assets/scss/main';
.main-wrapper{
  height: fit-content;
  position: relative;
  padding: 100px 0;
  .pattern{
    width: 300px;
    position: absolute;
    top:8%;
    right: 10%;
    z-index: -1;
  }
  .img-wrapper{
    width: 450px;
    height: 300px;
    overflow: hidden;
    img{
      width: 100%;
      object-fit: cover;
    }
  }
  .description-wrapper{
    background-color: white;
    width: 35%;
    min-width: 400px;
    height: fit-content;
    padding: 20px 55px;
    
    @media only screen and (min-width: 992px) {
      position: relative;
      right: 60px;
    }
      .line{
        border-bottom: 2px solid $main-orange;
        width: 50px;
        margin-bottom: 30px;      
      }
  }
  .nav-arrows{
    position: absolute;
    bottom: 0;
    left: 0;
      .my_btn{
        padding: 15px;
        margin:0;
      }
  }
  
}
</style>