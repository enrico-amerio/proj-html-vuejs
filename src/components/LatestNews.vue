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
         if(this.store.newsPage < 2){
           this.store.newsPage++
         }else{
           this.store.newsPage = 1
         }
       },
       goPrev(){
         if(this.store.newsPage > 1){
           this.store.newsPage--
         }else{
           this.store.newsPage = 2
        }
       }
    }
    
}
</script>

<template>
  <div class="container pt-5  text-center">
    <h3>Latest news</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <div class="line"></div>
  </div>
  <div class="container d-flex flex-wrap justify-content-center main-wrap pb-5" >
    <div class="my_container" v-for="news in this.data.latestNews" :key="news.id">
      <div class="carousel-wrap me-lg-3" v-if="this.store.newsPage == news.page ">
        <div class="img-wrap">
          <img :src="getPathImage(news.imgTop)" alt="newsImg1">
          <div class="img2">
            <img  :src="getPathImage(news.imgBottom)" alt="newsImg2">
          </div>
          <div class="tag">{{ news.tag }}</div>
        </div>
        <div class="info-wrap ">
          <p>
            <span>{{ news.date }}</span>
            <span>{{ news.author }}</span>
          </p>
          <h5>{{ news.title }}</h5>
          <p>{{ news.description }}</p>
          <a href="#">READ MORE</a>
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

.main-wrap{
  position: relative;
}
h3::after{
  content: '.';
  color: $main-orange;
}
.line{
      border-bottom: 2px solid $main-orange;
      width: 50px;
      margin: 0 auto;
      margin-bottom: 30px;      
    }
.img-wrap{
  max-width: 380px;
  height: 290px;
  position: relative;
  overflow: hidden;
  img{
    width:100%
  }
  .img2{
    position:absolute;
    left: 0;
    top: 0;
    height: 110px;
    overflow: hidden;
    
  }
  .tag{
    background-color: $main-orange;
    width: fit-content;
    padding: 5px 10px;
    color: white;
    position: absolute;
    right: 10px;
    bottom: 20px;
    font-weight: 200;
  }
}
.info-wrap{
 max-width: 380px;
  a{
    text-decoration: none;
    color:black;
    cursor: pointer;
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
</style>