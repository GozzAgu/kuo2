<template>
  <div ref="servicesSection" class="relative bg-gradient-to-r from-red-700 to-blue-700 h-[60vh] flex items-center justify-center text-white">
    <div class="relative z-10 text-center px-6 md:px-12 max-w-4xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-extrabold mb-4 transition-all duration-1000 ease-out transform opacity-0 translate-y-10"
        :class="{ 'opacity-100 translate-y-0': isVisible }">
        Our Services
      </h1>
      <p class="text-lg md:text-xl max-w-2xl mx-auto transition-all duration-1000 ease-out transform opacity-0 translate-y-10 delay-200"
        :class="{ 'opacity-100 translate-y-0': isVisible }">
        What we provide to our clients and customers
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const servicesSection = ref(null);
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

  if (servicesSection.value) {
    observer.observe(servicesSection.value);
  }
});
</script>

<style scoped>
</style>