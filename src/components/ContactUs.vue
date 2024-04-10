<script>
import {store} from '../data/store'
import slideJumbo from '../assets/db.json'

  export default {  
    data(){
      return{
        store,
        slideJumbo
      }
    },
}
</script>

<template>
  <div class="container d-flex pt-5 pb-5  ">
    <div class="col-xl-6 left">
      <img src="../assets/img/h1-contact-rev-01.png" alt="worldimg">
      <img class="pin" src="../assets/img/h1-contact-rev-02.png" alt="pin" id="pin1">
      <img class="pin" src="../assets/img/h1-contact-rev-02.png" alt="pin" id="pin2">
      <img class="pin" src="../assets/img/h1-contact-rev-02.png" alt="pin" id="pin3">
    </div>
    <div class="col-xl-6">
      <h3>Contact us</h3>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
      <div class="line"></div>
      <div class="row">
        <div class="col-12 col-lg-6">
          <div class="mb-3 ">
            <input type="text" class="form-control shadow-none" id="Inputname" placeholder="Your Name">
          </div>
        </div>
        <div class="col-12 col-lg-6">
          <div class="mb-3">
            <input type="text" class="form-control shadow-none" placeholder="Your Email">
          </div>
        </div>
        <div class="col-12">
          <div class="mb-3">
            <input type="text" class="form-control shadow-none message" placeholder="Write a message">
          </div>
          <a class="my_btn full">
            <div class="my-btn-title">SEND</div>
            <div class="my-btn-icon"><i class="fa-solid fa-arrow-right-long"></i></div>
          </a>
        </div>
      </div>
    </div>
  </div>
  <div class="container pt-4 pb-4">
    <div class="col-12 d-flex justify-content-between">
      <a><img src="../assets/img/h4-clients-img-03.png" alt="" class="logo"></a>
      <a><img src="../assets/img/h4-clients-img-05.png" alt="" class="logo"></a>
      <a><img src="../assets/img/h4-clients-img-07.png" alt="" class="logo"></a>
      <a><img src="../assets/img/h4-clients-img-09.png" alt="" class="logo"></a>
      <a><img src="../assets/img/h4-clients-img-01.png" alt="" class="logo"></a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.line{
  border-bottom: 2px solid $main-orange;
  width: 50px;
  margin-bottom: 30px;      
}
  h3::after{
    content: '.';
    color: $main-orange;
  }
.left{
  position: relative;
  .pin{
    position:absolute
  }
  #pin1{
    right: 75%;
    top:34%;
  }
  #pin2{
    right: 50%;
    top:20%;
  }
  #pin3{
    right: 20%;
    bottom:18%;
  }
}
.form-control{
  border:0px;
  border-bottom: 1px solid #e5e5e5 ;
  background-color: #fafafa ;
  &::placeholder {
  color: #A6A6A6;
  opacity: 1; 
}
&.message{
  padding-bottom: 50px;
}
}
.logo{
 width: 100px;
}
.logo:hover{
  filter: invert(45%) sepia(100%) saturate(4377%) hue-rotate(353deg) brightness(100%) contrast(102%);
}
</style>