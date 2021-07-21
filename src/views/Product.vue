<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <div class="row mb-3">
        <div class="col">
          <h3>Daftar <strong class="text-brown">Makanan</strong></h3>
        </div>
      </div>
      <div class="row mb-3">
        <div class="col-md-6">
          <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Enter your product keyword" aria-label="Enter your product keyword" aria-describedby="basic-addon2" v-model="search" @keyup="searchProduct()">
            <div class="input-group-append">
              <span class="input-group-text" id="basic-addon2"><b-icon-search></b-icon-search></span>
            </div>
          </div>
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
import CardProduct from "@/components/CardProduct.vue";

import axios from "axios";

export default {
  name: "Product",
  components: {
    Navbar,
    CardProduct,
  },
  data() {
    return {
      products: [],
      search: '',
    };
  },
  methods: {
    setProducts(data) {
      this.products = data;
    },
    searchProduct() {
      axios
      .get("http://localhost:3000/products?q="+this.search)
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log("Gagal : ", error));
    }
  },
  mounted() {
    // Make a request for a user with a given ID
    axios
      .get("http://localhost:3000/products")
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

<style>
</style>