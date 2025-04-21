<template>
  <section class="bg-[#f9f9f9] pt-20 pb-28">
    <div class="max-w-7xl mx-auto px-4">
      <h2 class="text-3xl font-bold text-gray-800 mb-10 text-center">
        Our Special Menu
      </h2>

      <!-- Wrap only scroll container + buttons -->
      <div class="relative">
        <!-- Left Arrow -->
        <button
          @click="scrollLeft"
          :class="[
            'absolute -left-6 top-1/2 -translate-y-1/2 z-10 w-10 h-10 rounded-full flex items-center justify-center shadow-md transition-colors',
            isAtStart ? 'bg-gray-300' : 'bg-[#ffa99f] hover:bg-[#ff998f]',
          ]"
        >
          ◀
        </button>

        <!-- Right Arrow -->
        <button
          @click="scrollRight"
          :class="[
            'absolute -right-6 top-1/2 -translate-y-1/2 z-10 w-10 h-10 rounded-full flex items-center justify-center shadow-md transition-colors',
            isAtEnd ? 'bg-gray-300' : 'bg-[#ffa99f] hover:bg-[#ff998f]',
          ]"
        >
          ▶
        </button>

        <!-- Products Scroll Area -->
        <div
          ref="scrollContainer"
          class="flex overflow-x-auto gap-6 scroll-smooth hide-scrollbar px-2 pb-8"
          @scroll="checkScroll"
        >
          <div
            v-for="(product, index) in products"
            :key="index"
            class="min-w-[250px] bg-white rounded-xl shadow-md p-4 relative flex flex-col items-center text-center"
          >
            <img
              :src="product.image"
              alt="Mie"
              class="w-40 h-40 rounded-full object-cover mb-4"
            />
            <div
              class="absolute top-4 right-4 bg-black text-white rounded-full w-8 h-8 flex items-center justify-center"
            >
              🛒
            </div>
            <h3 class="text-lg font-bold text-gray-800">{{ product.name }}</h3>
            <p class="text-sm text-gray-500 mb-2">{{ product.desc }}</p>
            <span class="text-md font-bold text-gray-800"
              >${{ product.price }}</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";

const scrollContainer = ref<HTMLElement | null>(null);
const isAtStart = ref(true);
const isAtEnd = ref(false);

const checkScroll = () => {
  const el = scrollContainer.value;
  if (!el) return;

  isAtStart.value = el.scrollLeft <= 0;
  isAtEnd.value = el.scrollLeft + el.offsetWidth >= el.scrollWidth - 10;
};

const scrollLeft = () => {
  if (scrollContainer.value) {
    scrollContainer.value.scrollBy({ left: -300, behavior: "smooth" });
  }
};

const scrollRight = () => {
  if (scrollContainer.value) {
    scrollContainer.value.scrollBy({ left: 300, behavior: "smooth" });
  }
};

onMounted(() => {
  checkScroll();
});

const products = [
  {
    name: "Mie Special 1",
    desc: "With Veggie Topping",
    price: "35.00",
    image:
      "https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg",
  },
  {
    name: "Mie Special 2",
    desc: "With Spicy Sauce",
    price: "35.00",
    image:
      "https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg",
  },
  {
    name: "Mie Special 3",
    desc: "With Boiled Egg",
    price: "35.00",
    image:
      "https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg",
  },
  {
    name: "Mie Special 4",
    desc: "With Sambal",
    price: "35.00",
    image:
      "https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg",
  },
  {
    name: "Mie Special 4",
    desc: "With Sambal",
    price: "35.00",
    image:
      "https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/08/02070057/Resep-Mie-Pedas-Level-Ala-Restoran-yang-Bisa-Dibuat-di-Rumah.jpg",
  },
];
</script>
<style scoped>
.hide-scrollbar::-webkit-scrollbar {
  display: none;
}
.hide-scrollbar {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
