<template>
  <section class="bg-[#f9f9f9] py-20">
    <div class="max-w-6xl mx-auto px-4">
      <!-- Title -->
      <h2 class="text-3xl md:text-4xl font-bold text-gray-800 text-center mb-4">
        Contact Me
      </h2>
      <p class="text-gray-500 text-center mb-12 max-w-lg mx-auto">
        Got a question or want to make a reservation? Just drop a message below.
      </p>

      <!-- Form and Map -->
      <div class="grid md:grid-cols-2 gap-10">
        <!-- Contact Form -->
        <form class="space-y-6">
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-1"
              >Email</label
            >
            <input
              type="email"
              placeholder="you@example.com"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500"
            />
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-1"
              >Pesan</label
            >
            <textarea
              rows="5"
              placeholder="Tulis pesanmu di sini..."
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500"
            ></textarea>
          </div>
          <button
            type="submit"
            class="bg-orange-600 hover:bg-orange-700 text-white px-6 py-3 rounded-full font-medium transition"
          >
            Kirim Pesan
          </button>
        </form>

        <!-- Map -->
        <div class="w-full h-[300px] rounded-lg overflow-hidden shadow-sm">
          <iframe
            class="w-full h-full"
            frameborder="0"
            allowfullscreen
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1983.877343458943!2d106.8271533!3d-6.1753945!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f3e9d8b4c1d7%3A0x1e398bb11a6d1b6!2sMonas!5e0!3m2!1sid!2sid!4v1682354357984!5m2!1sid!2sid"
          ></iframe>
        </div>
      </div>
    </div>
  </section>
</template>
