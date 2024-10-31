<template>
    <section class="bg-black text-gray-300 py-16 px-6 flex flex-col items-center text-center">
      <!-- Scrolling text effect (Let's Talk) -->
      <div class="w-full overflow-hidden mb-4">
        <div class="animate-marquee whitespace-nowrap text-gray-400 text-sm">
          <span class="mx-6">+++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++</span>
          <span class="mx-6">+++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++ LET'S TALK +++</span>
        </div>
      </div>
  
      <!-- Main Heading -->
      <div class="max-w-3xl">
        <p class="uppercase text-sm tracking-widest mb-6 text-gray-500">Project in mind?</p>
        <h1 class="text-5xl md:text-7xl font-bold text-gray-100 mb-4">Let’s make your</h1>
        <h1 class="text-5xl md:text-7xl font-light italic text-yellow-400 mb-6">Website shine</h1>
        <p class="text-gray-400 text-lg max-w-lg mx-auto mb-8">
          Premium web design, Webflow, and SEO services to help your business stand out.
        </p>
  
        <!-- Get In Touch Button -->
        <button class="bg-yellow-400 text-black py-3 px-6 rounded-full hover:bg-yellow-500 transition duration-200">
          Get In Touch
          <svg xmlns="http://www.w3.org/2000/svg" class="inline-block ml-2 h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
          </svg>
        </button>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'HeroSection',
  };
  </script>
  
  <style scoped>
  /* Marquee effect for scrolling text */
  @keyframes marquee {
    0% {
      transform: translateX(0%);
    }
    100% {
      transform: translateX(-100%);
    }
  }
  .animate-marquee {
    display: inline-block;
    animation: marquee 15s linear infinite;
  }
  </style>
  