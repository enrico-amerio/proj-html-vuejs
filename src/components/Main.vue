<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
  export default {
    data(){
      return{
        store
      }
    },
    components:{
      Specialities
    }
  }
</script>


<template>
  <Specialities/>
</template>



<style lang="scss" scoped>

</style>