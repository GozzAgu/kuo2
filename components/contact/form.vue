<template>
  <div class="bg-gray-100 py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <div class="text-center">
        <h2 class="text-3xl font-extrabold text-gray-700 sm:text-4xl">Get in Touch</h2>
        <p class="mt-4 text-lg text-gray-600">
          We'd love to hear from you! Reach out to us for any inquiries, collaborations, or just to say hello.
        </p>
      </div>

      <div class="mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div class="text-center bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex justify-center">
            <svg class="h-8 w-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a2 2 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Our Office</h3>
          <p class="mt-2 text-gray-600">
            No 85B, Elijiji Lane, Woji, Port-Harcourt, Rivers state, Nigeria
          </p>
        </div>

        <div class="text-center bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex justify-center">
            <svg class="h-8 w-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Call Us</h3>
          <p class="mt-2 text-gray-600">
            (+234) 811 484 9757<br>
            (+234) 818 962 7566
          </p>
        </div>

        <div class="text-center bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300">
          <div class="flex justify-center">
            <svg class="h-8 w-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Email Us</h3>
          <p class="mt-2 text-gray-600">
            info@kuosmartsolution.com<br>
            sales@kuosmartsolution.com<br>
            support@kuosmartsolution.com
          </p>
        </div>

        <div class="text-center bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300">
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Follow Us</h3>
          <div class="mt-4 flex justify-center space-x-4">
            <a href="#" class="text-gray-600 hover:text-blue-600">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-blue-600">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-blue-600">
              <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="#" class="text-gray-600 hover:text-blue-600">
              <i class="fab fa-instagram"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <section class="bg-white py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-3xl mx-auto">
      <h3 class="text-2xl font-bold text-gray-800 text-center">Send Us a Message</h3>
      <form class="mt-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <input type="text" placeholder="Full Name" class="w-full p-3 border rounded-lg focus:ring focus:ring-blue-300" required>
          <input type="email" placeholder="Email Address" class="w-full p-3 border rounded-lg focus:ring focus:ring-blue-300" required>
        </div>
        <input type="text" placeholder="Subject" class="w-full p-3 border rounded-lg mt-4 focus:ring focus:ring-blue-300" required>
        <textarea rows="5" placeholder="Your Message" class="w-full p-3 border rounded-lg mt-4 focus:ring focus:ring-blue-300" required></textarea>
        <button type="submit" class="mt-6 w-full bg-blue-600 text-white py-3 rounded-lg hover:bg-blue-700 transition">Send Message</button>
      </form>
    </div>
  </section>

  <section class="bg-gray-100 py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-5xl mx-auto">
      <h3 class="text-2xl font-bold text-gray-800 text-center mb-6">Find Us Here</h3>
      <div class="rounded-lg overflow-hidden shadow-lg">
        <iframe
          class="w-full h-96"
          frameborder="0"
          scrolling="no"
          marginheight="0"
          marginwidth="0"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3939.7626932203685!2d7.012478414294331!3d4.850387842309707!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1069cd57c3d4691d%3A0x6f5c6e60a445b20c!2sWoji%2C%20Port%20Harcourt%2C%20Rivers%2C%20Nigeria!5e0!3m2!1sen!2sng!4v1642024158442!5m2!1sen!2sng">
        </iframe>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css');
</style>
