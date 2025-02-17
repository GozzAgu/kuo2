<template>
  <div>
    <nav class="px-4 md:px-8 max-w-6xl py-4 border-b flex justify-between items-center mx-auto">
      <div class="text-xl font-bold text-gray-800">
        <router-link to="/">KUO Smart Solutions</router-link>
      </div>

      <div class="hidden md:flex space-x-8">
        <router-link to="/" class="nav-link" active-class="active-link">Home</router-link>
        <router-link to="/about" class="nav-link" active-class="active-link">About Us</router-link>
        <router-link to="/services" class="nav-link" active-class="active-link">Services</router-link>
        <router-link to="/projects" class="nav-link" active-class="active-link">Projects</router-link>
        <router-link to="/contact" class="nav-link" active-class="active-link">Contact</router-link>
      </div>

      <div class="hidden md:block">
        <router-link to="/get-started" class="bg-blue-600 text-white px-4 py-2 rounded-md hover:bg-blue-700 transition duration-300">
          Get Started
        </router-link>
      </div>

      <button @click="toggleMobileMenu" class="md:hidden focus:outline-none">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </nav>

    <div v-if="isMobileMenuOpen" class="fixed inset-0 bg-black bg-opacity-50 z-50 md:hidden" @click="toggleMobileMenu"></div>
    <div :class="['fixed inset-y-0 right-0 w-64 bg-white z-50 transform transition-transform duration-300 ease-in-out', isMobileMenuOpen ? 'translate-x-0' : 'translate-x-full']">
      <div class="p-4">
        <button @click="toggleMobileMenu" class="text-gray-600 hover:text-gray-900 focus:outline-none">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
      </div>
      <div class="flex flex-col space-y-4 p-4">
        <router-link to="/" class="nav-link" active-class="active-link">Home</router-link>
        <router-link to="/about" class="nav-link" active-class="active-link">About Us</router-link>
        <router-link to="/services" class="nav-link" active-class="active-link">Services</router-link>
        <router-link to="/projects" class="nav-link" active-class="active-link">Projects</router-link>
        <router-link to="/contact" class="nav-link" active-class="active-link">Contact</router-link>
        <router-link to="/get-started" class="bg-blue-600 text-white px-4 py-2 rounded-md hover:bg-blue-700 transition duration-300 text-center">
          Get Started
        </router-link>
      </div>
    </div>

    <div>
      <slot />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};
</script>

<style scoped>
.nav-link {
  @apply text-gray-600 hover:text-gray-900 transition duration-300 ease-in-out;
  position: relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -2px;
  left: 0;
  background-color: #1a73e8;
  transition: width 0.3s ease-in-out;
}

.nav-link:hover::after {
  width: 100%;
}

.active-link {
  @apply text-blue-600 font-semibold;
}

.active-link::after {
  width: 100%;
}
</style>