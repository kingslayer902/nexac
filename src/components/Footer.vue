<template>
  <footer class="bg-blue-900 text-white py-8 px-6">
    <div class="max-w-6xl mx-auto grid md:grid-cols-3 gap-8 text-center md:text-left">
      <!-- Branding -->
      <div>
        <h3 class="text-xl font-bold text-yellow-300 mb-2">NexAC</h3>
        <p class="text-sm text-gray-300">
          Solusi terbaik pemasangan dan pembelian AC untuk rumah & kantor Anda.
        </p>
      </div>

      <!-- Kontak -->
      <div>
        <h4 class="text-md font-semibold mb-2">Hubungi Kami</h4>
        <p class="text-sm">WhatsApp: <a href="https://wa.me/6289636446722" target="_blank" class="underline">0896-3644-6722</a></p>
        <p class="text-sm">Email: nexac@email.com</p>
        <p class="text-sm">Jam Operasional: 08.00 - 21.00 WIB</p>
      </div>

      <!-- Navigasi -->
      <div>
        <h4 class="text-md font-semibold mb-2">Navigasi</h4>
        <ul class="space-y-1">
          <li><router-link to="/" class="hover:underline text-sm">Beranda</router-link></li>
          <li><router-link to="/product" class="hover:underline text-sm">Produk</router-link></li>
          <li><router-link to="/jasa" class="hover:underline text-sm">Jasa</router-link></li>
          <li><router-link to="/about" class="hover:underline text-sm">Tentang Kami</router-link></li>
        </ul>
      </div>
    </div>

    <div class="mt-8 text-center text-sm text-gray-400 border-t border-white/20 pt-4">
      &copy; 2025 NexAC. All rights reserved.
    </div>
  </footer>
</template>
