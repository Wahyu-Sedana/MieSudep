<template>
  <nav class="bg-white border-b border-gray-200 shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="text-2xl font-bold text-orange-600">MieSudep</div>

        <!-- Navigation Links -->
        <ul class="hidden md:flex space-x-8 text-gray-700 font-medium">
          <li>
            <a href="#" class="hover:text-orange-600 transition">Home</a>
          </li>
          <li>
            <a href="#menu" class="hover:text-orange-600 transition">Menu</a>
          </li>
          <li>
            <a href="#about" class="hover:text-orange-600 transition">About</a>
          </li>
          <li>
            <a href="#contact" class="hover:text-orange-600 transition"
              >Contact</a
            >
          </li>
        </ul>

        <!-- CTA or Mobile Menu Button Placeholder -->
        <div class="md:hidden">
          <!-- You can place a hamburger icon here later -->
          <button class="text-gray-700 hover:text-orange-600">☰</button>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts"></script>
