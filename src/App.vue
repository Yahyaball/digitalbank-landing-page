<script setup lang="ts">
import Header from '@/components/Header.vue';
import Home from '@/components/Home.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
  <Header />
  <div id="page-content" ref="pageContent">
    <Home />
    <Footer />
  </div>
</template>
