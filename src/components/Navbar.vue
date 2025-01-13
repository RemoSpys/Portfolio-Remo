<template>
  <div class="sticky top-0 z-50 bg-gray-900 bg-opacity-90 p-4 shadow-lg flex justify-between items-center">
    <router-link
      to="/"
      class="font-bold text-xl text-blue-400 hover:text-blue-500 transition"
    >
      Remo.S
    </router-link>
    <div class="md:hidden flex items-center">
      <button
        @click="toggleMenu"
        class="text-blue-400 hover:text-blue-500 focus:outline-none transition"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3 5h18M3 12h18M3 19h18"
          />
        </svg>
      </button>
    </div>

    <!-- Desktop Menu -->
    <div class="hidden md:flex items-center space-x-8">
      <router-link
        v-for="link in links"
        :key="link.name"
        :to="link.href"
        class="flex items-center text-gray-300 hover:text-blue-400 hover:underline transition"
      >
        <i :class="link.icon + ' mr-2'"></i>
        {{ link.name }}
      </router-link>
      <button
        @click="navigateToContact"
        class="flex items-center text-gray-300 hover:text-blue-400 font-bold p-2 rounded-xl hover:underline transition"
      >
        <i class="fas fa-comment-dots mr-2"></i>
        Let's talk
      </button>
      <a
        :href="cvFile"
        download="Remo.pdf"
        class="flex items-center text-gray-300 hover:text-blue-400 font-bold p-2 rounded-xl hover:underline transition"
      >
        <i class="fas fa-file-download mr-2"></i>
        Download CV
      </a>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="isMenuOpen"
      class="fixed inset-0 bg-gray-900 bg-opacity-90 z-50 p-6 flex flex-col space-y-6 md:hidden rounded-lg"
    >
      <router-link
        v-for="link in links"
        :key="link.name"
        :to="link.href"
        @click.stop="closeMenu"
        class="flex items-center text-gray-300 text-lg hover:underline hover:text-blue-400 transition"
      >
        <i :class="link.icon + ' mr-2'"></i>
        {{ link.name }}
      </router-link>
      <button
        @click="navigateToContact"
        class="flex items-center text-gray-300 font-bold rounded-xl hover:underline transition"
      >
        <i class="fas fa-comment-dots mr-2"></i>
        Let's talk
      </button>
      <a
        :href="cvFile"
        download="Remo.pdf"
        class="flex items-center text-gray-300 font-bold rounded-xl hover:underline transition"
      >
        <i class="fas fa-file-download mr-2"></i>
        Download CV
      </a>
      <button
        @click="closeMenu"
        class="absolute top-4 right-4 text-gray-300 hover:text-blue-400"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      links: [
        { name: "Home", href: "/", icon: "fas fa-home" },
        { name: "Services", href: "/services", icon: "fas fa-briefcase" },
        { name: "About", href: "/about", icon: "fas fa-info-circle" },
      ],
      isMenuOpen: false,
      cvFile: "path/to/Remo.pdf", // Replace with the actual path to your PDF file
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    },
    navigateToContact() {
      this.$router.push("/contact");
      this.isMenuOpen = false;
    },
  },
};
</script>

<style scoped>
.bg-gray-900 {
  background-color: #1f2937;
}

.bg-opacity-90 {
  background-color: rgba(31, 41, 55, 0.9);
}

.text-blue-400 {
  color: #60a5fa;
}

.text-blue-400:hover {
  color: #3b82f6;
}

.text-gray-300 {
  color: #d1d5db;
}

.text-gray-300:hover {
  color: #9ca3af;
}

.hover\:underline:hover {
  text-decoration: underline;
}

.fixed.inset-0 {
  width: 100%;
  height: 100%;
}

.rounded-b-lg {
  border-bottom-left-radius: 0.75rem;
  border-bottom-right-radius: 0.75rem;
}

.shadow-lg {
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.3);
}
</style>
