<script>
import {store} from '../../data/store'
export default {
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <div class="card-wrapper">
    <h4 class="title">Upcoming Events</h4>
    <div class="event d-flex">
      <div class="calendar col-4 d-flex flex-column align-content-center justify-content-center ">
        <div class="calendar-wrapper text-center">
          <h5 class="day">07</h5>
          <p class="date">Jan, 2022</p>
        </div>
      </div>
      <div class="event-info col-8">
        <h6 class="event-name ">Melbourne Coaching</h6>
        <p class="event-tim ">9:00 18:00 ciaociao</p>
        <p class="event-location ">via giovanni ciao</p>
        <h6>READ MORE</h6>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;
.card-wrapper{
  border: 1px solid black;
  width: 300px;
  margin-bottom: 100px;
  .title{
    border-bottom:1px solid black;
  }
  .calendar-wrapper{
    background-color: $main-orange;
    color: white;
    p{
      color: white;
    }
  }
  
}
</style>