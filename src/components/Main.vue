<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
import Events from './Events.vue';
import LatestNews from './LatestNews.vue';
import CreativeLeader from './CreativeLeader.vue';
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
      Events,
      CreativeLeader,
      LatestNews
    }
  }
</script>


<template>
  <Specialities/>
  <Staff/>
  <Events/>
  <CreativeLeader/>
  <LatestNews/>
</template>



<style lang="scss" scoped>

</style>