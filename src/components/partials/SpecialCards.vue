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
      status : String,
    }
  };
</script>

<template>
  <div class="card m-3 text-center " style="width: 18rem;">
    <img :src="img" class="card-img-top" :alt="title" tabindex="0">
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-title">{{ description }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card{
  text-align: center;
  border: 0;
}
</style>