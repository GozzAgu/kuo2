<template>
  <div ref="heroSection" class="relative bg-gradient-to-r from-red-700 to-blue-700 h-[60vh] flex items-center justify-center text-white">
    <div class="relative z-10 text-center px-6 md:px-12 max-w-4xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-extrabold mb-4 transition-all duration-1000 ease-out transform opacity-0 translate-y-10"
        :class="{ 'opacity-100 translate-y-0': isVisible }">
        Get in Touch With Us
      </h1>
      <p class="text-lg md:text-xl max-w-2xl mx-auto transition-all duration-1000 ease-out transform opacity-0 translate-y-10 delay-200"
        :class="{ 'opacity-100 translate-y-0': isVisible }">
        Have questions, inquiries, or collaboration ideas? We're here to help! Reach out and let’s create something amazing together.
      </p>
      <div class="mt-6 transition-all duration-1000 ease-out transform opacity-0 translate-y-10 delay-400"
        :class="{ 'opacity-100 translate-y-0': isVisible }">
        <a href="#contact-form" class="bg-white text-blue-700 font-semibold px-6 py-3 rounded-lg shadow-lg hover:bg-gray-100 transition duration-300">
          Contact Us
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const heroSection = ref(null);
const isVisible = ref(false);

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          isVisible.value = true;
          observer.unobserve(entry.target);
        }
      });
    },
    { threshold: 0.5 }
  );

  if (heroSection.value) {
    observer.observe(heroSection.value);
  }
});
</script>

<style scoped>
</style>