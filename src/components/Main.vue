<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
import Events from './Events.vue';
import Staff from './Staff.vue';

  export default {
    data(){
      return{
        store
      }
    },
    components:{
      Specialities,
      Staff,
      Events
    }
  }
</script>


<template>
  <Specialities/>
  <Staff/>
  <Events/>
</template>



<style lang="scss" scoped>

</style>