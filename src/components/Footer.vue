<template>
  <div class="wrapper">
    <footer class="bg-blue-300 text-black py-4 w-full">
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
  </div>
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

.wrapper {
  min-height: calc(100vh - 60px); /* Adjust 60px according to your header height */
  display: flex;
  flex-direction: column;
}

footer {
  margin-top: auto;
}
</style>
