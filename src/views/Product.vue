<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <h1>Daftar Product</h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";

export default {
  name: "Product",
  components: {
    Navbar,
  },
};
</script>

<style>
</style>