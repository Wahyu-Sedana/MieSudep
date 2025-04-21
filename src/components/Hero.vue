<template>
  <section
    class="max-w-7xl mx-auto flex flex-col-reverse md:flex-row items-center justify-between px-4 md:px-8 py-16 md:py-24 bg-white"
  >
    <!-- Left: Text -->
    <div class="md:w-1/2 space-y-5 text-center md:text-left">
      <h1
        class="text-4xl md:text-5xl font-semibold text-gray-900 leading-tight"
      >
        it's not just <br />
        <span class="font-bold">Food, It’s an Experience.</span>
      </h1>
      <div
        class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start mt-4"
      >
        <a
          href="/menu"
          class="bg-orange-600 hover:bg-orange-700 text-white font-medium px-6 py-3 rounded-full transition"
        >
          View Menu
        </a>
        <a
          href="/booking"
          class="bg-gray-100 hover:bg-gray-200 text-gray-800 font-medium px-6 py-3 rounded-full transition"
        >
          Book a Table
        </a>
      </div>
      <!-- Reviews -->
      <div class="mt-6 flex items-center justify-center md:justify-start gap-3">
        <div class="flex -space-x-2">
          <img
            src="https://i.pravatar.cc/40?img=10"
            class="w-9 h-9 rounded-full border-2 border-white"
          />
          <img
            src="https://i.pravatar.cc/40?img=12"
            class="w-9 h-9 rounded-full border-2 border-white"
          />
          <img
            src="https://i.pravatar.cc/40?img=14"
            class="w-9 h-9 rounded-full border-2 border-white"
          />
        </div>
        <span class="text-sm text-gray-600">★★★★★ 4.9 (200+ reviews)</span>
      </div>
    </div>

    <!-- Right: Image -->
    <div class="md:w-1/2 flex justify-center mb-10 md:mb-0 relative">
      <img
        src="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg"
        alt="Mie lezat"
        class="w-[340px] h-[340px] md:w-[400px] md:h-[400px] object-cover rounded-full shadow-xl"
      />

      <div
        class="absolute top-4 right-4 bg-red-100 text-red-600 text-xs md:text-sm px-3 py-1 rounded-full shadow font-medium"
      >
        🔥 5% Off Today
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>
