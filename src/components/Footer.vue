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
  <div class="wrapper">
    <div class="container">
      <div class="row">
        <div class="col">
          <h6>About</h6>
          <div class="line"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt cupiditate reiciendis sequi consectetur modi ut ipsam placeat sed quam odit voluptas praesentium velit, magni debitis, error dicta, inventore cum ratione et minima! Natus sint nemo nobis doloribus optio.</p>
          <div class="icon-wrap">
            <a href="#" class="social-icon"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#" class="social-icon"><i class="fa-brands fa-twitter"></i></a>
          </div>
        </div>
        <div class="col">
          <h6>Twitter</h6>
          <div class="line"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus eum ad aut reiciendis, nulla asperiores explicabo ullam necessitatibus optio! Veritatis!</p>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Autem, vitae ad sed nihil asperiores obcaecati debitis ratione sequi sunt perspiciatis!</p>
        </div>
        <div class="col">
          <h6>Important links</h6>
          <div class="line"></div>
          <ul>
            <li><a href="">About me</a></li>
            <li><a href="">About us</a></li>
            <li><a href="">Language packs</a></li>
            <li><a href="">Become a coach</a></li>
            <li><a href="">Monthly event</a></li>
          </ul>
        </div>
        <div class="col">
          <h6>Contact me</h6>
          <div class="line"></div>
          <ul>
            <li>457 BigBlue Street, NY 10013</li>
            <li>(315) 5512-2579</li>
            <li>everlead@mikado.com</li>
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
  p{
    color: white;
  }
}
</style>