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
  }
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="row">
        <div class="col">
          <h6>About</h6>
          <div class="line"></div>
          <p>{{ this.data.footer.bio }}</p>
          <div class="icon-wrap">
            <a href="#" class="social-icon"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-twitter"></i></a>
          </div>
        </div>
        <div class="col">
          <h6>Twitter</h6>
          <div class="line"></div>
          <p v-for="post in this.data.footer.twitter" :key="post.id">{{ post.post }}</p>
        </div>
        <div class="col">
          <h6>Important links</h6>
          <div class="line"></div>
          <ul>
            <li v-for="link in this.data.footer.importantLinks" :key="link.id"><a href="">{{link.name}}</a></li>
            
          </ul>
        </div>
        <div class="col-12 col-xl-3">
          <h6>Contact me</h6>
          <div class="line"></div>
          <ul>
            <li><i class="fa-solid fa-location-dot"></i> {{ this.data.footer.contacts.address }}</li>
            <li><i class="fa-solid fa-phone"></i> {{ this.data.footer.contacts.phone }}</li>
            <li><i class="fa-solid fa-envelope"></i> {{ this.data.footer.contacts.mail }}</li>
          </ul>
          <input type="text" placeholder="Your Name" class="form-control shadow-none">
        </div>
      </div>
    </div>
  </div>
  <div class="col copyright">
    <p>Copyright Everlead Mikado Layout</p>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.wrapper{
  padding: 100px 0;
  background-color: #181515;
  color:white;
  .line{
    border-bottom: 1px solid $main-orange;
    width: 30px;
    margin-bottom: 30px;      
  }
  ul, li { margin: 0;
    padding: 0;
    list-style-type: none;
    font-weight: 300;
    i{
      color: $main-orange;
      margin-right: 5px;
    }  
  }
  a{
    text-decoration: none;
    color: white;
    cursor: pointer;
  }
  .form-control{
    border:0px;
    border-bottom: 1px solid #e5e5e5 ;
    background-color: #181515 ;
    &::placeholder {
    color: #A6A6A6;
    opacity: 1; 
  }
  }
  .social-icon{
    background-color: white;
    color: #181515 ;
  }
}
.copyright{
  background-color:$main-orange ;
  text-align: center;
  height: fit-content;
  p{
    color: white;
    margin:0;
  }
}
</style>