<template>
  <section class="py-16 px-4 bg-gray-50 min-h-screen">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-blue-800 mb-10">
        Daftar Produk AC Terbaru
      </h2>

      <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <CardProduct
          v-for="p in productStore.products"
          :key="p.id"
          :product="p"
        />
      </div>

      <div v-if="productStore.products.length === 0" class="text-center text-gray-600 mt-10">
        <p>Produk belum tersedia untuk saat ini.</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import { useProductStore } from '../stores/productStore'
import CardProduct from '../components/CardProduct.vue'

const productStore = useProductStore()

onMounted(() => {
  productStore.fetchProducts()
})
</script>
