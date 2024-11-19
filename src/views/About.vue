<template>
  <section
    class="bg-gradient-to-b from-gray-800 to-gray-900 py-20 px-6 md:px-10"
  >
    <div class="flex flex-col items-center justify-center min-h-screen">
      <!-- Main Header Section -->
      <div class="text-center">
        <h1 class="text-5xl md:text-6xl font-serif text-white">
          <span
            class="italic text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-cyan-600"
          >
            RemoSpys
          </span>
        </h1>
        <p class="pt-4 text-2xl font-light text-gray-300">
          A Web Designer, Developer, and Game Developer Bringing Almost Every
          Idea to Life!
        </p>
      </div>

      <!-- About Me Button Section -->
      <div class="mt-8">
        <button
          class="flex items-center justify-center text-white bg-gradient-to-r from-cyan-400 to-cyan-600 hover:from-cyan-500 hover:to-cyan-700 py-3 px-6 rounded-full shadow-lg transition-all duration-300"
          @click="toggleAboutMe"
        >
          <span class="mr-2">Want to Know More About Me?</span>
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
              d="M19 9l-7 7-7-7"
            />
          </svg>
        </button>
      </div>

      <!-- About Me Section (Revealed on Button Click) -->
      <div v-if="showAboutMe" class="mt-12 text-center px-6 md:px-10">
        <div class="flex justify-center items-center w-full">
          <div
            class="relative w-full md:w-2/3 lg:w-1/2 px-6 py-8 bg-gray-800 border border-gray-600 rounded-2xl shadow-lg hover:shadow-2xl transition duration-300"
          >
            <p
              class="uppercase tracking-widest text-xs font-semibold text-cyan-500 mb-3"
            >
              Web Design Expert
            </p>

            <h2 class="text-3xl md:text-4xl font-extrabold text-white mb-6">
              Crafting Websites and Game Development that Speak for Your Brand
            </h2>

            <p class="text-gray-400 font-semibold leading-relaxed mb-6">
              Hi! I'm RemoSpys, a highly skilled web designer, developer, and
              game developer. I combine creativity with cutting-edge technology
              to bring almost any idea to life. Whether it's a stunning website
              or custom scripts for games like FiveM, Rust, DayZ, or Minecraft,
              I specialize in crafting interactive, highly functional solutions
              tailored just for you.
            </p>

            <p class="text-gray-400 font-semibold leading-relaxed mb-6">
              Collaboration is at the heart of my process. I take the time to
              listen to your ideas and ensure that the final product not only
              looks great but functions perfectly across all platforms. I focus
              on making your vision come true with clean, intuitive, and
              user-friendly designs.
            </p>

            <p class="text-gray-400 font-semibold leading-relaxed mb-6">
              As a developer, I love pushing the boundaries of what’s possible.
              Whether it's building complex game scripts that enhance the player
              experience or creating seamless animations for websites, I always
              strive to deliver results that exceed expectations.
            </p>

            <p class="text-gray-400 font-semibold leading-relaxed">
              Ready to create something amazing together? Let's turn your ideas
              into reality, whether it's a website or a custom game server.
            </p>
          </div>
        </div>
      </div>
      <!-- Call-to-Action Section -->
      <div class="text-center px-6 md:px-10 mt-16">
        <p class="uppercase tracking-widest text-slate-400 text-xl">
          Let's Build Your Digital Future
        </p>
        <h1 class="text-4xl md:text-7xl font-semibold mt-4 text-slate-100">
          Ready to Start Your <br />
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-cyan-600 italic"
            >Website</span
          >
          or
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-cyan-600 italic"
            >Game Script</span
          >
          Journey?
        </h1>
        <p class="mt-6 text-xl text-slate-300 max-w-xl mx-auto pb-20">
          Premium web design, development, and game scripting services to help
          your business and projects stand out with creativity and innovation.
        </p>
        <router-link
          to="/contact"
          class="mt-8 px-8 py-4 bg-gradient-to-r from-cyan-400 to-cyan-600 hover:from-cyan-500 hover:to-cyan-700 font-light rounded-lg shadow-lg transition duration-300 ease-in-out transform hover:scale-105"
        >
          Get In Touch
        </router-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showAboutMe: false,
    }
  },
  methods: {
    toggleAboutMe() {
      this.showAboutMe = !this.showAboutMe
    },
  },
}
</script>

<style scoped>
#about {
  transition:
    opacity 0.5s ease,
    transform 0.3s ease;
}
</style>
