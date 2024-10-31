<template>
  <footer class="bg-black text-gray-400 py-12 px-6">
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-4 gap-8">
      <!-- Social Links Section -->
      <div class="flex flex-col space-y-6 items-start">
        <h3 class="text-lg font-semibold text-gray-300">Follow Us</h3>
        <div class="flex flex-col space-y-4">
          <a href="#" class="flex items-center space-x-4 hover:text-white transition">
            <div class="w-8 h-8 rounded-full border border-gray-400"></div>
            <span class="text-sm">Instagram</span>
          </a>
          <a href="#" class="flex items-center space-x-4 hover:text-white transition">
            <div class="w-8 h-8 rounded-full border border-gray-400"></div>
            <span class="text-sm">Twitter</span>
          </a>
          <a href="#" class="flex items-center space-x-4 hover:text-white transition">
            <div class="w-8 h-8 rounded-full border border-gray-400"></div>
            <span class="text-sm">Dribbble</span>
          </a>
          <a href="#" class="flex items-center space-x-4 hover:text-white transition">
            <div class="w-8 h-8 rounded-full border border-gray-400"></div>
            <span class="text-sm">Behance</span>
          </a>
        </div>
      </div>

      <!-- Pages Links -->
      <div>
        <h3 class="text-lg font-semibold text-gray-300">Pages</h3>
        <ul class="space-y-2 mt-4">
          <li><a href="#" class="hover:text-white transition">Home</a></li>
          <li><a href="#" class="hover:text-white transition">Services</a></li>
          <li><a href="#" class="hover:text-white transition">About</a></li>
          <li><a href="#" class="hover:text-white transition">Contact</a></li>
        </ul>
      </div>

      <!-- CMS Links -->
      <div>
        <h3 class="text-lg font-semibold text-gray-300">CMS</h3>
        <ul class="space-y-2 mt-4">
          <li><a href="#" class="hover:text-white transition">Work</a></li>
          <li><a href="#" class="hover:text-white transition">Work Single</a></li>
          <li><a href="#" class="hover:text-white transition">Blog</a></li>
          <li><a href="#" class="hover:text-white transition">Blog Post</a></li>
        </ul>
      </div>

      <!-- Utility Pages Links -->
      <div>
        <h3 class="text-lg font-semibold text-gray-300">Utility Pages</h3>
        <ul class="space-y-2 mt-4">
          <li><a href="#" class="hover:text-white transition">404 Error Page</a></li>
          <li><a href="#" class="hover:text-white transition">Password Protected</a></li>
          <li><a href="#" class="hover:text-white transition">Styleguide</a></li>
          <li><a href="#" class="hover:text-white transition">Licensing</a></li>
          <li><a href="#" class="hover:text-white transition">Changelog</a></li>
        </ul>
      </div>
    </div>

    <!-- Footer Bottom -->
    <div class="mt-12 border-t border-gray-700 pt-8 flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0">
      <p class="text-sm text-gray-500">© 2024 Made by Remo S. Powered by Vue.js.</p>
      <a href="#" @click.prevent="scrollToTop" class="flex items-center space-x-2 text-sm hover:text-white transition cursor-pointer">
        <span>To Top</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 15l7-7 7 7" />
        </svg>
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      });
    },
  },
};
</script>

<style scoped>
/* Responsive and cleaner styles for mobile */
footer {
  font-family: 'Nippo', sans-serif; /* Match font if needed */
}

footer a {
  font-size: 0.875rem; /* Make links smaller and cleaner */
}

footer h3 {
  letter-spacing: 0.05em; /* Add spacing to headings for a refined look */
}

footer .border {
  background-color: transparent;
}

footer ul li a:hover {
  transition: all 0.2s ease-in-out;
}

footer svg {
  stroke-width: 1.5;
  transition: transform 0.2s ease;
}

footer svg:hover {
  transform: translateY(-2px);
}

/* Adjust padding and spacing for mobile */
@media (max-width: 768px) {
  footer {
    padding: 16px;
  }

  footer .container {
    grid-template-columns: 1fr;
    gap: 16px;
  }

  footer .border-t {
    margin-top: 2rem;
  }
}
</style>
