<template>
  <section class="px-6 md:px-12 py-12 max-w-6xl mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
        Our Products
      </h2>
    </div>
    <div class="bg-gray-100 mt-6 p-6 rounded-lg">
      <h3 class="text-lg font-semibold text-gray-800 mb-4">Security Seals</h3>

      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
        <div v-for="product in products" :key="product.id" class="bg-white p-4 rounded-lg">
          <img :src="product.image" alt="Product image" class="w-full h-32 object-contain mb-4">
          <h4 class="font-semibold text-gray-900">{{ product.name }}</h4>
          <p class="text-gray-600 text-sm">{{ product.description }}</p>
          <p class="text-gray-500 text-xs mt-2">MOQ: <span class="font-medium">{{ product.moq }}</span></p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const products = [
  { id: 1, name: "Plastic seal + nylon insert", description: "Tamper proof high security cable seal", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
  { id: 2, name: "Cable seal", description: "Tamper evident plastic security seal for container", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
  { id: 3, name: "Plastic seal + metal insert", description: "High quality security cable safety locks container seal", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
  { id: 4, name: "Cable seal", description: "ABS + steel line", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
  { id: 5, name: "Cable seal", description: "Alloy + steel line", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
  { id: 6, name: "Plastic seal + metal locking", description: "PP + steel", moq: "1,000 Pieces", image: "https://via.placeholder.com/100" },
];
</script>

<style scoped>
</style>
