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
