<template>
  <div>
    <!-- Splash Screen -->
    <transition name="fade">
      <div
        v-if="showSplash"
        class="fixed inset-0 bg-white z-50 flex flex-col items-center justify-center"
      >
        <div class="text-4xl font-bold text-orange-600 animate-pulse">
          MieSudepp
        </div>
        <p class="text-gray-500 mt-2">Loading your taste...</p>
      </div>
    </transition>

    <!-- Main App Content -->
    <div v-show="!showSplash">
      <RouterView />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";

const showSplash = ref(true);

onMounted(() => {
  setTimeout(() => {
    showSplash.value = false;
  }, 2000); // Splash screen tampil 2 detik
});
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.8s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
