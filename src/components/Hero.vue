<template>
  <div class="hero">
    <!-- Desktop Version -->
    <div class="d-md-block d-none">
      <div class="row mt-4">
        <div class="col-md-7">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong
                  >Best
                  <span class="text-brown">Americano Coffee,</span> </strong
                ><br />in Jakarta Indonesia
              </h2>
              <p>
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                since 1500s
              </p>
              <router-link to="/product" class="btn btn-lg btn-success">
                Order Now <b-icon-arrow-right></b-icon-arrow-right>
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-5">
          <img src="../assets/images/hero.svg" width="100%" alt="" />
        </div>
      </div>
    </div>

    <!-- Mobile Version -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4 d-sm-block d-sm-none">
        <div class="col-md-5 mb-4">
          <img src="../assets/images/hero.svg" width="100%" alt="" />
        </div>
        <div class="col-md-7">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong
                  >Best
                  <span class="text-brown">Americano Coffee,</span> </strong
                ><br />in Jakarta Indonesia
              </h2>
              <p>
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                since 1500s
              </p>
              <button class="btn btn-lg btn-success">
                Order Now <b-icon-arrow-right></b-icon-arrow-right>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>