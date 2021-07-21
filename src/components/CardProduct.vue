<template>
  <div class="card shadow card-border mb-5" style="100%">
    <img
      :src="'images/product/' + productz.gambar"
      class="card-img-top"
      alt="..."
    />
    <div class="card-body">
      <h5 class="card-title">{{ productz.nama }}</h5>
      <p class="card-text">Harga : Rp {{ productz.harga }}</p>
      <a href="#" class="btn btn-success"
        >Order Now <b-icon-cart></b-icon-cart
      ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["productz"],
};
</script>

<style>
</style>