<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
import Events from './Events.vue';
import Testimonials from './Testimonials.vue';
import Video from './Video.vue';
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
      LatestNews,
      Testimonials,
      Video
    }
  }
</script>


<template>
  <Specialities/>
  <Staff/>
  <Events/>
  <CreativeLeader/>
  <LatestNews/>
  <Testimonials/>
  <Video/>
</template>



<style lang="scss" scoped>

</style>