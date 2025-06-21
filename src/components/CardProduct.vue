<template>
  <div class="bg-white rounded-xl shadow hover:shadow-xl transition p-5 flex flex-col justify-between">
    <img
      :src="product.gambar"
      :alt="product.nama"
      class="w-full h-48 object-cover rounded-lg mb-4 border"
    />
    <h3 class="text-lg font-semibold mb-1 text-gray-800">{{ product.nama }}</h3>
    <p class="text-sm text-gray-600 mb-2">{{ product.deskripsi }}</p>
    <p class="text-blue-700 font-bold mb-4 text-base">
      Rp{{ product.harga.toLocaleString('id-ID') }}
    </p>
    <a
      :href="`https://wa.me/6289636446722?text=Halo%20NexAC!%20Saya%20tertarik%20dengan%20${encodeURIComponent(product.nama)}%20seharga%20Rp${product.harga.toLocaleString('id-ID')}.%20Masih%20tersedia?`"
      target="_blank"
      class="bg-gradient-to-r from-blue-600 to-blue-700 text-white py-2 px-4 rounded-lg text-center hover:scale-105 hover:from-blue-700 hover:to-blue-800 transition-all duration-300"
    >
      Beli via WhatsApp
    </a>
  </div>
</template>

<script setup>
defineProps(['product'])
</script>
