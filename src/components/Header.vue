<script>
import {store} from '../data/store'
import Nav from './partials/Nav.vue'

  export default {  
    components:{
      Nav
    },
    data(){
      return{
        store
      }
    },
    
    
  }
</script>


<template>
  <Nav/>
 

</template>



<style lang="scss" scoped>

</style>