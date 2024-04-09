<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
import Staff from './Staff.vue';
  export default {
    data(){
      return{
        store
      }
    },
    components:{
      Specialities,
      Staff
    }
  }
</script>


<template>
  <Specialities/>
  <Staff/>
</template>



<style lang="scss" scoped>

</style>