<template>
  <footer class="bg-gray-900 text-gray-400 py-12 px-6">
    <div class="container mx-auto grid grid-cols-1 md:grid-cols-4 gap-8">
      <div class="flex flex-col space-y-6 items-start">
        <h3 class="text-lg font-semibold text-gray-300">Follow Me</h3>
        <div class="flex flex-col space-y-4">
          <!-- GitHub Link -->
          <a
            href="https://github.com/RemoSpys"
            target="_blank"
            class="flex items-center space-x-4 hover:text-gray-100 transition"
          >
            <div
              class="w-8 h-8 flex items-center justify-center rounded-full border border-gray-600"
            >
              <Icon icon="mdi:github" class="h-6 w-6" />
            </div>
            <span class="text-sm">GitHub</span>
          </a>

          <!-- Discord Link -->
          <div
            @click="showDiscord"
            class="flex items-center space-x-4 hover:text-gray-100 transition cursor-pointer"
          >
            <div
              class="w-8 h-8 flex items-center justify-center rounded-full border border-gray-600"
            >
              <Icon icon="ic:baseline-discord" class="h-6 w-6" />
            </div>
            <span class="text-sm">Discord</span>
          </div>

          <!-- LinkedIn Link -->
          <a
            href="https://www.linkedin.com/in/remo-tammela-046861339/"
            target="_blank"
            class="flex items-center space-x-4 hover:text-gray-100 transition"
          >
            <div
              class="w-8 h-8 flex items-center justify-center rounded-full border border-gray-600"
            >
              <Icon icon="mdi:linkedin" class="h-6 w-6" />
            </div>
            <span class="text-sm">LinkedIn</span>
          </a>
        </div>
      </div>

      <div>
        <h3 class="text-lg font-semibold text-gray-300">Pages</h3>
        <ul class="space-y-2 mt-4">
          <li>
            <a href="/home" class="hover:text-gray-100 transition">Home</a>
          </li>
          <li>
            <a href="/services" class="hover:text-gray-100 transition"
              >Services</a
            >
          </li>
          <li>
            <a href="/about" class="hover:text-gray-100 transition">About</a>
          </li>
          <li>
            <a href="/contact" class="hover:text-gray-100 transition"
              >Contact</a
            >
          </li>
        </ul>
      </div>
    </div>

    <div
      class="mt-12 border-t border-gray-700 pt-8 flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0"
    >
      <p class="text-sm text-gray-500">
        © 2024 Made by Remo S. Powered by Vue.js.
      </p>
      <a
        href="#"
        @click.prevent="scrollToTop"
        class="flex items-center space-x-2 text-sm hover:text-gray-100 transition cursor-pointer"
      >
        <span>To Top</span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-4 w-4"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M5 15l7-7 7 7"
          />
        </svg>
      </a>
    </div>
  </footer>
</template>

<script>
import { Icon } from '@iconify/vue'

export default {
  name: 'Footer',
  components: {
    Icon,
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      })
    },
    showDiscord() {
      alert('Add me on Discord: RemoSpys')
    },
  },
}
</script>

<style scoped>
footer {
  font-family: 'Nippo', sans-serif;
}

footer a {
  font-size: 0.875rem;
  color: inherit;
}

footer h3 {
  letter-spacing: 0.05em;
}

footer .border {
  background-color: transparent;
}

footer ul li a:hover {
  transition: all 0.2s ease-in-out;
  color: inherit;
}

footer svg {
  stroke-width: 1.5;
  transition: transform 0.2s ease;
}

footer svg:hover {
  transform: translateY(-2px);
}

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
