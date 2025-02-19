<template>
  <div>
    <nav class="px-4 md:px-8 max-w-6xl py-4 border-b flex justify-between items-center mx-auto">
      <div class="text-xl font-bold text-gray-800">
        <router-link to="/">
          <img
            src="/public/kuologo.png"
            alt="LOGO"
            class="w-24 md:w-32"
          />
        </router-link>
      </div>

      <div class="hidden md:flex space-x-8">
        <router-link to="/" class="nav-link" active-class="active-link">Home</router-link>
        <router-link to="/about" class="nav-link" active-class="active-link">About Us</router-link>
        <router-link to="/services" class="nav-link" active-class="active-link">Services</router-link>
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

    <footer class="bg-gray-800 text-white py-12">
      <div class="max-w-6xl mx-auto px-4 md:px-8">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
          <div class="mb-8 md:mb-0">
            <h3 class="text-xl font-bold mb-4">About KUO</h3>
            <p class="text-gray-400 leading-relaxed">
              KUO Smart Solutions is a leading provider of industrial solutions, specializing in electrical, instrumentation, and automation systems. We are committed to innovation, quality, and customer satisfaction.
            </p>
          </div>

          <div class="mb-8 md:mb-0">
            <h3 class="text-xl font-bold mb-4">Quick Links</h3>
            <ul class="space-y-2">
              <li><router-link to="/" class="text-gray-400 hover:text-blue-500 transition duration-300">Home</router-link></li>
              <li><router-link to="/about" class="text-gray-400 hover:text-blue-500 transition duration-300">About Us</router-link></li>
              <li><router-link to="/services" class="text-gray-400 hover:text-blue-500 transition duration-300">Services</router-link></li>
              <li><router-link to="/contact" class="text-gray-400 hover:text-blue-500 transition duration-300">Contact</router-link></li>
            </ul>
          </div>

          <div class="mb-8 md:mb-0">
            <h3 class="text-xl font-bold mb-4">Contact Us</h3>
            <ul class="space-y-2">
              <li class="text-gray-400">No 85B, Elijiji Lane, Woji, Port-Harcourt, Rivers state, Nigeria.</li>
              <li class="text-gray-400">Email: info@kuosmartsolution.com</li>
              <li class="text-gray-400">Phone: (+234) 811 484 9757</li>
            </ul>
          </div>

          <div>
            <h3 class="text-xl font-bold mb-4">Follow Us</h3>
            <div class="flex space-x-4">
              <a href="https://facebook.com" target="_blank" class="text-gray-400 hover:text-blue-500 transition duration-300">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z" />
                </svg>
              </a>
              <a href="https://twitter.com" target="_blank" class="text-gray-400 hover:text-blue-500 transition duration-300">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z" />
                </svg>
              </a>
              <a href="https://linkedin.com" target="_blank" class="text-gray-400 hover:text-blue-500 transition duration-300">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                </svg>
              </a>
              <a href="https://instagram.com" target="_blank" class="text-gray-400 hover:text-blue-500 transition duration-300">
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
                </svg>
              </a>
            </div>
          </div>
        </div>

        <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
          &copy; 2023 KUO Smart Solutions. All rights reserved.
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isMobileMenuOpen = ref(false);
const route = useRoute()

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

watch(
  () => route.path,
  () => {
    isMobileMenuOpen.value = false;
  }
);
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