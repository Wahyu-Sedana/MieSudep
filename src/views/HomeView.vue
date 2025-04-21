<template>
  <Navbar />
  <Hero />
  <ProductList />
  <WhyChooseUs />
  <ContactUs />
  <footer class="bg-white border-t border-gray-200 py-10">
    <div
      class="max-w-7xl mx-auto px-4 flex flex-col md:flex-row justify-between items-start md:items-center gap-10 md:gap-0"
    >
      <!-- Left: Logo + Description -->
      <div>
        <div class="text-2xl font-bold text-orange-600 mb-2">MieSudepp</div>
        <p class="text-gray-500 text-sm max-w-xs">
          Mie khas Nusantara yang bikin nagih — rasa lokal, tampilan global.
        </p>
      </div>

      <!-- Center: Navigation -->
      <div
        class="flex flex-col md:flex-row items-start md:items-center gap-4 text-gray-600 text-sm font-medium"
      >
        <a href="#" class="hover:text-orange-600 transition">Home</a>
        <a href="#menu" class="hover:text-orange-600 transition">Menu</a>
        <a href="#about" class="hover:text-orange-600 transition">About</a>
        <a href="#contact" class="hover:text-orange-600 transition">Contact</a>
      </div>

      <!-- Right: Social Media -->
      <div class="flex gap-4 text-gray-500">
        <a href="#" class="hover:text-orange-600 transition text-xl">🌐</a>
        <a href="#" class="hover:text-orange-600 transition text-xl">📷</a>
        <a href="#" class="hover:text-orange-600 transition text-xl">🐦</a>
      </div>
    </div>

    <!-- Bottom -->
    <div class="text-center text-sm text-gray-400 mt-10">
      &copy; 2025 MieSudepp. All rights reserved.
    </div>
  </footer>
</template>

<script setup lang="ts">
import Navbar from "../components/Navbar.vue";
import Hero from "../components/Hero.vue";
import ProductList from "../components/ProductList.vue";
import WhyChooseUs from "../components/WhyChooseUs.vue";
import ContactUs from "../components/ContactUs.vue";
</script>
