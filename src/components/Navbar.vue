<template>
  <nav class="bg-white shadow-md px-6 py-4 flex justify-between items-center sticky top-0 z-50">
    <h1 class="text-xl font-bold text-blue-700 tracking-wide">NexAC</h1>

    <!-- Hamburger / Close button -->
    <button @click="toggleMenu" class="md:hidden text-gray-700 focus:outline-none z-50 relative">
      <svg v-if="!menuOpen" xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/>
      </svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" class="w-7 h-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
      </svg>
    </button>

    <!-- Navigation Links -->
    <transition name="slide-fade">
      <ul
        :class="[
          'md:flex md:items-center md:gap-6 text-sm font-semibold text-gray-700',
          menuOpen
            ? 'absolute top-16 left-0 w-full bg-white shadow-md flex flex-col space-y-4 px-6 py-4 md:static md:space-y-0 md:flex-row md:bg-transparent md:shadow-none'
            : 'hidden md:flex'
        ]"
      >
        <li><router-link to="/" class="hover:text-blue-600 transition-colors">Beranda</router-link></li>
        <li><router-link to="/product" class="hover:text-blue-600 transition-colors">Produk</router-link></li>
        <li><router-link to="/jasa" class="hover:text-blue-600 transition-colors">Jasa</router-link></li>
        <li><router-link to="/about" class="hover:text-blue-600 transition-colors">Tentang</router-link></li>
      </ul>
    </transition>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}
</script>

<style scoped>
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
