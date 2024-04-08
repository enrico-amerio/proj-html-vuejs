<script>
import {store} from '../../data/store'
  export default {  
    data(){
      return{
        store
      }
    },
    
  }
</script>


<template>
  <nav class="navbar navbar-expand-lg ">
  <div class="container">
    <div class="col-6">
      <a class="navbar-brand" href="#">
        <img src="../../assets/img/logo-img-01.png" alt="Everlead-logo" class="logo">
      </a>
    </div>
    <div class="col-6">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0  ">
          <li class="nav-item">
            <a class="nav-link" href="#">HOMES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">PAGES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">BLOG</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">SHOP</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">EVENTS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">ELEMENTS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fa-solid fa-list-ul"></i></a>
          </li>
        </ul>
      </div>
      
    </div>
  </div>
</nav>
</template>



<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as * ;
nav{
  position:fixed;
  z-index: 999;
  width: 100%;
    .logo{
      width: 100px;
    }
    .nav-link{
      font-size:10px;
      font-weight: 700;
      &:hover{
        color: $main-orange;
        &::before{
          content:'\f178';
          font-family: 'Font Awesome 5 Free';
          margin: 8px;
        }
      }
    }
}
</style>