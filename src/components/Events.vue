<script>
import {store} from '../data/store'
import data from '../assets/db.json'

export default {
  data(){
      return{
        store,
        data
      }
    },
    methods: {
      getDayFromDate(dateString) {
      const day = dateString.split(',')[1].trim().split(' ')[1];
      return parseInt(day);
    },
    
  }

}
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="card-wrapper">
    <h5 class="title">Upcoming Events</h5>
    <div class="event d-flex" v-for="event in data.events" :key="event.id">
      <div class="calendar col-4 d-flex flex-column align-content-center justify-content-center ">
        <div class="calendar-wrapper text-center">
          <h5 class="day">{{ getDayFromDate(event.date) }}</h5>
          <p class="date">Jan, 2022</p>
        </div>
      </div>
      <div class="event-info col-8">
        <h6 class="event-name ">{{ event.title }}</h6>
        <p class="event-tim ">{{event.date}}</p>
        <p class="event-location ">{{event.location}}</p>
        <a>READ MORE</a>
      </div>
    </div>
  </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.wrapper{
  //  position: relative;
    width: 100%;
    display: flex;
    align-items:center ;
    
    background-image:url('../assets/img/h1-img-09.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 900px;
    
    
  .card-wrapper{
    background-color: #fafafa ;
    // position:absolute;
    // top: 20%;
    // left: 20%;
    border: 1px solid #e1e1e1;
    width: 300px;
    margin-bottom: 100px;
    height: fit-content;
    margin: 0 auto;
    @media only screen and (min-width: 1200px) {
      margin: 0 15%;
      
    }
    
    
    .title, .event{
      border-bottom:1px solid #e1e1e1;
    }
    .title{
      height: 50px;
      text-align: center;
      line-height: 50px;
    }
    .event{
      &:hover{
        background-color: white;
      }
      .event-info{
        padding: 10px;
      }
      h6, a{
        font-size: 0.8rem;
        
      }
      a{
        cursor: pointer;
        

      }
      p{
        font-size: 0.6rem;
      }
    }
    .event:last-of-type{
      border: 0;
    }
    .calendar-wrapper{
      background-color: $main-orange;
      height: fit-content;
      width: fit-content;
      padding: 10px;
      margin: 0 auto;
      p, h5{
        color: white;
        margin: 0;
        
      }
    }
}
  
}
</style>