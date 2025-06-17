<template>
  <section class="min-h-screen bg-gradient-to-br from-blue-500 to-blue-800 text-white px-6 py-16">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-4xl md:text-5xl font-extrabold mb-4 drop-shadow">Selamat Datang di <span class="text-yellow-300">NexAC</span></h1>
      <p class="text-lg md:text-xl mb-6">Solusi Terpercaya untuk Pemasangan & Pembelian AC Anda</p>
      <div class="flex flex-col md:flex-row gap-4 justify-center">
        <router-link
          to="/product"
          class="bg-white text-blue-700 px-6 py-3 rounded font-semibold shadow hover:bg-blue-100 transition"
        >
          Lihat Produk
        </router-link>
        <a
          href="https://wa.me/6289636446722?text=Halo%20NexAC!%20Saya%20tertarik%20dengan%20layanan%20Anda."
          target="_blank"
          class="bg-green-500 hover:bg-green-600 text-white px-6 py-3 rounded font-semibold transition"
        >
          Hubungi via WhatsApp
        </a>
      </div>
    </div>

    <!-- Fitur Unggulan -->
    <div class="mt-20 grid md:grid-cols-3 gap-8 max-w-6xl mx-auto text-center">
      <div class="bg-white/10 p-6 rounded-lg shadow hover:bg-white/20 transition">
        <h3 class="text-xl font-semibold mb-2">Teknisi Berpengalaman</h3>
        <p class="text-sm text-gray-200">Ditangani oleh teknisi profesional dan bersertifikat.</p>
      </div>
      <div class="bg-white/10 p-6 rounded-lg shadow hover:bg-white/20 transition">
        <h3 class="text-xl font-semibold mb-2">Layanan Cepat</h3>
        <p class="text-sm text-gray-200">Pemesanan cepat, pemasangan dalam 24 jam.</p>
      </div>
      <div class="bg-white/10 p-6 rounded-lg shadow hover:bg-white/20 transition">
        <h3 class="text-xl font-semibold mb-2">Garansi Terjamin</h3>
        <p class="text-sm text-gray-200">Garansi hingga 1 tahun untuk layanan dan unit AC.</p>
      </div>
    </div>
  </section>
</template>
