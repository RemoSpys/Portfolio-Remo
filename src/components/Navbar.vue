<template>
  <div class="flex justify-center mt-4">
    <nav class="animated-navbar flex flex-col md:flex-row items-center space-y-4 md:space-y-0 md:space-x-8 text-white p-2 bg-gray-800 bg-opacity-60 border-gray-700 border rounded-lg shadow-lg">
      <div class="flex justify-between w-full md:w-auto items-center">
        <!-- Logo and Brand Name with Hover Animation -->
        <h3 class="font-bold text-2xl text-gray-300 transition-transform duration-300 hover:scale-105">Remo S.</h3>

        <!-- Mobile Menu Toggle Button -->
        <button @click="toggleMenu" class="md:hidden focus:outline-none">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 text-gray-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        </button>
      </div>

      <!-- Desktop Menu Links with Slide Hover Effect -->
      <div class="hidden md:flex flex-row items-center space-x-8">
        <a href="#services" class="nav-link">Services</a>
        <a href="#work" class="nav-link">Work</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#blog" class="nav-link">Blog</a>
        <a href="#pages" class="nav-link">Pages</a>
        <button class="bg-gray-700 text-gray-200 px-4 py-2 rounded-lg hover:bg-gray-600 transition-colors duration-200">Let's Talk</button>
      </div>

      <!-- Mobile Dropdown Menu with Animation -->
      <transition name="slide-fade" mode="out-in">
        <div v-if="isMenuOpen" class="flex flex-col space-y-4 w-full items-center md:hidden mt-4">
          <a href="#services" @click="closeMenu" class="hover:underline hover:text-gray-400 transition-colors duration-200">Services</a>
          <a href="#work" @click="closeMenu" class="hover:underline hover:text-gray-400 transition-colors duration-200">Work</a>
          <a href="#about" @click="closeMenu" class="hover:underline hover:text-gray-400 transition-colors duration-200">About</a>
          <a href="#blog" @click="closeMenu" class="hover:underline hover:text-gray-400 transition-colors duration-200">Blog</a>
          <a href="#pages" @click="closeMenu" class="hover:underline hover:text-gray-400 transition-colors duration-200">Pages</a>
          <button @click="closeMenu" class="bg-gray-700 text-gray-200 px-4 py-2 rounded-lg hover:bg-gray-600 transition-colors duration-200">Let's Talk</button>
        </div>
      </transition>
    </nav>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Navbar',
  setup() {
    const isMenuOpen = ref(false);
    const toggleMenu = () => (isMenuOpen.value = !isMenuOpen.value);
    const closeMenu = () => (isMenuOpen.value = false);

    return { isMenuOpen, toggleMenu, closeMenu };
  },
};
</script>

<style scoped>
/* Navbar Fade-in Animation */
.animated-navbar {
  opacity: 0;
  transform: translateY(-10px);
  animation: fadeInSlide 0.5s ease-out forwards;
}

@keyframes fadeInSlide {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Slide and fade transition for mobile dropdown */
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter-from {
  transform: translateY(-10px);
  opacity: 0;
}
.slide-fade-enter-to {
  transform: translateY(0);
  opacity: 1;
}
.slide-fade-leave-from {
  transform: translateY(0);
  opacity: 1;
}
.slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}

/* Slide hover effect for desktop nav links */
.nav-link {
  position: relative;
  padding-bottom: 4px;
  transition: color 0.3s ease;
}
.nav-link::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 2px;
  background-color: #4b5563;
  transition: width 0.3s ease;
}
.nav-link:hover {
  color: #a0aec0;
}
.nav-link:hover::after {
  width: 100%;
}
</style>
