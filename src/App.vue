<template>
  <div class="flex flex-col min-h-screen">
    <Navbar />
    
    <main class="flex-grow">
      <router-view />
    </main>
    
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<style>
body {
  font-family: 'Inter', sans-serif;
  background-color: #f9fafb; /* warna dasar abu muda */
  margin: 0;
}
</style>
