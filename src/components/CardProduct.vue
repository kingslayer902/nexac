<template>
  <div class="bg-white rounded shadow hover:shadow-lg transition p-4 flex flex-col justify-between">
    <img :src="product.gambar" :alt="product.nama" class="w-full h-48 object-cover rounded mb-4" />
    <h3 class="text-lg font-semibold mb-1">{{ product.nama }}</h3>
    <p class="text-sm text-gray-600 mb-2">{{ product.deskripsi }}</p>
    <p class="text-blue-700 font-bold mb-4">Rp{{ product.harga.toLocaleString('id-ID') }}</p>
    <a
      :href="`https://wa.me/6289636446722?text=Halo, saya tertarik dengan ${product.nama} seharga Rp${product.harga.toLocaleString('id-ID')}. Apakah masih tersedia?`"
      target="_blank"
      class="bg-blue-600 text-white py-2 px-4 rounded text-center hover:bg-blue-700 transition"
    >
      Beli via WhatsApp
    </a>
  </div>
</template>

<script setup>
defineProps(['product'])
</script>
