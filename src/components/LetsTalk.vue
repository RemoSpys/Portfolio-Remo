<template>
  <section class="py-24 px-6 bg-yellow-200 text-gray-900 flex flex-col items-center">
    <!-- Scrolling Text -->
    <div class="w-full overflow-hidden text-center mb-8">
      <div class="scrolling-text text-sm font-semibold uppercase text-gray-700 whitespace-nowrap">
        +++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++
      </div>
    </div>

    <!-- Heading and Subtitle -->
    <div class="text-center mb-12">
      <p class="text-sm uppercase tracking-widest text-gray-700 mb-2">Project in Mind?</p>
      <h2 class="text-5xl font-light italic">Let’s make your</h2>
      <h1 class="text-7xl font-bold italic mb-4">Website shine</h1>
      <p class="text-lg font-light text-gray-700">Premium web design, webflow, and SEO services to help your business stand out.</p>
    </div>

    <!-- Call-to-Action Button -->
    <button class="flex items-center bg-gray-800 text-white px-6 py-3 rounded-lg hover:bg-gray-700 transition duration-300">
      GET IN TOUCH
      <svg xmlns="http://www.w3.org/2000/svg" class="ml-2 w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
      </svg>
    </button>
  </section>
</template>

<script>
export default {
  name: 'LetsTalk',
};
</script>

<style scoped>
.scrolling-text {
  display: inline-block;
  animation: scroll-text 10s linear infinite;
}

@keyframes scroll-text {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}
</style>
