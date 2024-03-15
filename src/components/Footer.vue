<template>
  <footer class="bg-gray-800 text-gray-300 py-4 absolute bottom-0 w-full">
    <div class="container mx-auto px-10 flex justify-between items-center">
      <!-- Left side with copyright info -->
      <div class="text-sm">
        <p>&copy; {{ currentYear }} Vanilla</p>
      </div>

      <!-- Middle section with developed by information -->
      <div class="text-sm">
        <p>
          Developed By
          <a href="https://chiraitori.lol" class="text-blue-400 hover:underline">Chiraitori</a>
        </p>
      </div>

      <!-- Right side with social icons -->
      <div class="flex space-x-4">
        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-facebook"></i></a>
        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-twitter"></i></a>
        <a href="#" class="text-gray-300 hover:text-white"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
/* You may need to include Tailwind's base styles and fontawesome styles */

/* Example Tailwind base styles */
@import 'tailwindcss/base';

/* Example Font Awesome styles */
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css');
</style>
