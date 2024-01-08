<template>
  <nav>
    <Header/>
    <router-view/>
    <Footer/>
  </nav>
</template>

<script setup>
import Header from "@/components/Shared/Header.vue";
import Footer from "@/components/Shared/Footer.vue";


</script>

<style>


* {
  margin: 0;
}

body {
  font-family: "Raleway", Helvetica, sans-serif;
  color: #444;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: Helvetica;
}

a {
  text-decoration: none;
  color: #fff;
}
</style>