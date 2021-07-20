<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <h1>This is about page.</h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";

export default {
  name: "About",
  components: {
    Navbar,
  },
};
</script>

<style>
</style>