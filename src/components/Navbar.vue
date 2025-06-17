<template>
  <nav class="bg-white shadow-md px-6 py-4 flex justify-between items-center sticky top-0 z-50">
    <h1 class="text-xl font-bold text-blue-700">NexAC</h1>

    <!-- Hamburger menu untuk mobile -->
    <button @click="toggleMenu" class="md:hidden text-gray-700 focus:outline-none">
      <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24"
           stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round"
              d="M4 6h16M4 12h16M4 18h16"/>
      </svg>
    </button>

    <!-- Menu navigasi -->
    <ul
      :class="[
        'md:flex md:items-center md:gap-6 text-sm font-semibold text-gray-700',
        menuOpen ? 'block absolute top-16 left-0 w-full bg-white shadow-md md:static md:bg-transparent md:shadow-none' : 'hidden md:flex'
      ]"
    >
      <li class="px-6 py-2 md:px-0 md:py-0"><router-link to="/">Home</router-link></li>
      <li class="px-6 py-2 md:px-0 md:py-0"><router-link to="/product">Produk</router-link></li>
      <li class="px-6 py-2 md:px-0 md:py-0"><router-link to="/jasa">Jasa</router-link></li>
      <li class="px-6 py-2 md:px-0 md:py-0"><router-link to="/about">About</router-link></li>
    </ul>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}
</script>
