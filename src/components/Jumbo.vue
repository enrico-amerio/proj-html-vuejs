<script>
import {store} from '../data/store'
import slideJumbo from '../assets/db.json'

  export default {  
    data(){
      return{
        store,
        slideJumbo
      }
    },
    methods:{
      getPathImage(img){
        return new URL(`../assets/img/${img}`, import.meta.url).href
      },
      goNext(){
        if(this.store.jumboCounter < this.slideJumbo.slideJumbo.length){
          this.store.jumboCounter++
        }else{
          this.store.jumboCounter = 1
        }
      },
      goPrev(){
        if(this.store.jumboCounter > 1){
          this.store.jumboCounter--
        }else{
          this.store.jumboCounter = this.slideJumbo.slideJumbo.length
        }
      }
    }
    
    
  }
</script>


<template>
  <div class="wrapper" >
    <div v-for="slide in slideJumbo.slideJumbo" :key="slide.id" class="slide">
      <div v-if="this.store.jumboCounter == slide.id" >
        <img :src="getPathImage(slide.img)" alt="jumboImg">
        <div class="d-flex flex-column justify-content-center container">
          <div class="infoJumbo">
            <h1>{{ slide.title }}</h1>
            <p>{{ slide.description }}</p>
            <div class="btn-wrapper d-flex">
              <a class="my_btn light" v-if="slide.btn1">
                <div class="my-btn-title">{{ slide.btn1 }}</div>
                <div class="my-btn-icon"><i class="fa-solid fa-arrow-right-long"></i></div>
              </a>
              <a class="my_btn full" v-if="slide.btn2">
                <div class="my-btn-title">{{ slide.btn2 }}</div>
                <div class="my-btn-icon"><i class="fa-solid fa-arrow-right-long"></i></div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="nav-arrows container d-flex justify-content-between">
      <a @click="goPrev"><i class="fa-solid fa-arrow-left-long"></i></a>
      <a @click="goNext"><i class="fa-solid fa-arrow-right-long"></i></a>
    </div>
  </div>


</template>



<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.wrapper{
  position: relative;
   display: flex;
  flex-direction: column;
  align-items: center; 
  .slide{
    position: relative;
    width: 100%;
    z-index: -1;
    
    img{
      width: 100%;
      height: 90vh;
      max-height: 1000px;
      // z-index: -2;
          object-fit: cover;
        }
        .infoJumbo{
          width: 30%;
          position: absolute;
          left: 18%;
          top: 40%;
          
          h1::after{
            content: '.';
            color: $main-orange;
          }
        }
      }
      .nav-arrows{
        position: absolute;
        top:50%;
        margin: 0 auto;
        z-index: 2;
        a{
          cursor: pointer;
        }
      }

}
      
</style>