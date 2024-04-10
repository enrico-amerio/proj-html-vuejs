<script>
export default {

}
</script>

<template>
  <div class="wrapper p-5">
    <div class="container  mt-5">
      <div class="col-xl-6 mb-5">
        <h3> Creative Leader</h3>
        <div class="line"></div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis molestias maxime sequi labore incidunt ipsam ducimus, consequatur numquam voluptatum quos!</p>
        <a href="#" class="">READ MORE</a>
      </div>
      <div class="col-xl-6">
        <div class="info-wrap d-flex justify-content-between ">
          <h6>Mentorship</h6>
          <h6>78%</h6>
        </div>
        <div class="progress mb-4 " role="progressbar" aria-label="Example 1px high" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" style="height: 2px">
          <div class="progress-bar" style="width: 78%"></div>
        </div>
        <div class="info-wrap d-flex justify-content-between ">
          <h6>Education</h6>
          <h6>95%</h6>
        </div>
        <div class="progress mb-4" role="progressbar" aria-label="Example 1px high" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" style="height: 2px">
          <div class="progress-bar" style="width: 95%"></div>
        </div>
        <div class="info-wrap d-flex justify-content-between ">
          <h6>Learning</h6>
          <h6>65%</h6>
        </div>
        <div class="progress mb-4" role="progressbar" aria-label="Example 1px high" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" style="height: 2px">
          <div class="progress-bar" style="width: 65%"></div>
        </div>
        <div class="info-wrap d-flex justify-content-between ">
          <h6>Motivation</h6>
          <h6>83%</h6>
        </div>
        <div class="progress mb-4 " role="progressbar" aria-label="Example 1px high" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" style="height: 2px">
          <div class="progress-bar" style="width: 83%"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/main';
@use '../assets/scss/partials/variables' as * ;
.wrapper{
  width: 100%;
  height: fit-content;
  background-color:white ;
  padding: 25px 0;
  .container{
    @media only screen and (min-width: 992px) {
      display: flex;
      
    }
  }
  h3::after{
      content: '.';
      color: $main-orange;
    }
  .line{
        border-bottom: 2px solid $main-orange;
        width: 50px;
        margin-bottom: 30px;      
      }
  a{
    text-decoration: none;
    color: black;
    cursor: pointer;
    font-weight: 500;
  }
  .progress-bar{
    background-color: $main-orange;
  }
}

</style>