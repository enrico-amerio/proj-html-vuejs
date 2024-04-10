<script>
import {store} from '../data/store';
import Specialities from './Specialities.vue';
import Events from './Events.vue';
import Testimonials from './Testimonials.vue';
import Video from './Video.vue';
import LatestNews from './LatestNews.vue';
import ContactUs from './ContactUs.vue'
import CreativeLeader from './CreativeLeader.vue';
import Staff from './Staff.vue';
import ContactUsVue from './ContactUs.vue';

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
      Video,
      ContactUs
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
  <ContactUs/>
</template>



<style lang="scss" scoped>

</style>