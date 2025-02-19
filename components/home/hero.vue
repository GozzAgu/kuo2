<template>
  <div>
    <div ref="heroSection" class="relative bg-cover bg-center h-[80vh] flex items-center justify-center text-white">
      <div class="absolute inset-0 bg-black bg-opacity-50"></div>
      <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')] bg-cover bg-center"></div>

      <div class="relative z-10 text-center px-4 md:px-8 max-w-4xl mx-auto flex flex-col gap-6">
        <h1 class="text-4xl md:text-6xl font-bold transition-all duration-1000 ease-in-out transform translate-y-20 opacity-0" :class="{'translate-y-0 opacity-100': isVisible}">
          Balancing the Equation
        </h1>
        <p class="text-lg md:text-2xl transition-all duration-1000 ease-in-out transform translate-y-20 opacity-0 delay-200" :class="{'translate-y-0 opacity-100': isVisible}">
          Meeting Demand and Supply with Precision and Expertise.
        </p>
        <a
          href="/get-started"
          class="bg-blue-600 text-white px-8 py-3 rounded-md text-lg font-semibold hover:bg-blue-700 transition duration-300 transform translate-y-20 opacity-0 delay-400" :class="{'translate-y-0 opacity-100': isVisible}"
        >
          Get Started
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
    {
      threshold: 0.5,
    }
  );

  if (heroSection.value) {
    observer.observe(heroSection.value);
  }
});
</script>

<style scoped>

</style>