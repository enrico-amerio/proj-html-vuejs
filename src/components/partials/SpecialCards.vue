<script>
import {store} from '../../data/store'
import specialities from '../../assets/db.json'
  export default {
    data(){
      return{
        store,
        specialities
      }
    },
    props:{
      img: String,
      title: String,
      description : String,
    }
  };
</script>

<template>
  <div class="card m-3 text-center d-flex flex-column align-items-center " style="width: 12em;">
    <img :src="img" class="card-img-top" :alt="title">
    <div class="card-body">
      <h6 class="card-title">{{ title }}</h6>
      <p class="card-title">{{ description }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/main';
@use '../../assets/scss/partials/variables' as * ;
.card{

  text-align: center;
  border: 0;
    img{
      filter: invert(45%) sepia(100%) saturate(4377%) hue-rotate(353deg) brightness(100%) contrast(102%);
      width: 40%;
    }
    p{
      font-size: 0.8rem;
    }
    
}
</style>