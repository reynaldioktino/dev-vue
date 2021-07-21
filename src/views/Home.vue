<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />
      <br /><br />
      <div class="row mt-5 mb-2">
        <div class="col">
          <h4><strong>Best </strong>Product List</h4>
        </div>
        <div class="col">
          <router-link to="/product" class="btn btn-success float-right btn-sm"
            >See All <b-icon-eye></b-icon-eye
          ></router-link>
        </div>
      </div>

      <div class="row mb-3">
        <div
          class="col-md-4 mt-d"
          v-for="productx in products"
          :key="productx.id"
        >
          <CardProduct :productz="productx" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";

import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProducts(data) {
      this.products = data;
    },
  },
  mounted() {
    // Make a request for a user with a given ID
    axios
      .get("http://localhost:3000/best-products")
      .then((response) =>
        // handle success
        // console.log("Berhasil : ", response);
        this.setProducts(response.data)
      )
      .catch((error) =>
        // handle error
        console.log("Gagal : ", error)
      );
  },
};
</script>
