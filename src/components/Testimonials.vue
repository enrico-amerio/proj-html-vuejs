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
         if(this.store.testimonialCounter < this.data.testimonials.length){
           this.store.testimonialCounter++
         }else{
           this.store.testimonialCounter = 1
         }
       },
       goPrev(){
         if(this.store.testimonialCounter > 1){
           this.store.testimonialCounter--
         }else{
           this.store.testimonialCounter = this.data.testimonials.length
         }
       }
    }
  }
</script>

<template>
  <div class="wrapper ">
    <div class="container" v-for="testimonial in data.testimonials" :key="testimonial.id">
      <div class="testimonial text-center " v-if="testimonial.id == this.store.testimonialCounter">
        <img class="mb-3" :src="getPathImage(testimonial.img)" alt="testimonial">
        <h6>{{ testimonial.name }}</h6>
        <p>{{ testimonial.description }}</p>
      </div>
    </div>
    <div class="nav-arrows container d-flex justify-content-between">
      <a @click="goPrev"><i class="fa-solid fa-arrow-left-long"></i></a>
      <a @click="goNext"><i class="fa-solid fa-arrow-right-long"></i></a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  padding: 100px 0;
  background-color: #1e1c1c;
  height: fit-content;
  width: 100%;
  color:white;
  position:relative;
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