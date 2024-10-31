<template>
  <section class="py-24 px-6 bg-black text-white flex flex-col items-center">
    <!-- Centered Icon Grid -->
    <div class="grid grid-cols-4 md:grid-cols-8 lg:grid-cols-12 gap-6 justify-center mb-12 max-w-screen-lg">
      <i class="devicon-html5-plain colored text-6xl"></i>
      <i class="devicon-tailwindcss-plain colored text-6xl"></i>
      <i class="devicon-lua-plain colored text-6xl"></i>
      <i class="devicon-python-plain colored text-6xl"></i>
      <i class="devicon-javascript-plain colored text-6xl"></i>
      <i class="devicon-css3-plain colored text-6xl"></i>
      <i class="devicon-java-plain colored text-6xl"></i>
      <i class="devicon-mysql-plain colored text-6xl"></i>
      <i class="devicon-windows8-original colored text-6xl"></i> <!-- Representing PowerShell -->
      <i class="devicon-php-plain colored text-6xl"></i>
      <i class="devicon-bash-plain colored text-6xl"></i>
      <i class="devicon-cplusplus-plain colored text-6xl"></i>
    </div>

    <!-- Service Descriptions Grid -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-screen-md">
      <div class="p-6 border border-gray-600 hover:bg-gray-900 transition rounded-lg">
        <h2 class="text-lg font-semibold mb-4">01 WEB DESIGN</h2>
        <p class="text-gray-400 mb-6">Visually stunning web designs that captivate your audience by blending your brand voice and customer needs.</p>
        <a href="#" class="flex items-center text-sm text-gray-300 hover:text-white">
          ABOUT WEBDESIGN
          <svg class="ml-2 w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
            <path d="M12.293 3.293a1 1 0 011.414 0l5 5a1 1 0 01-1.414 1.414L14 6.414V17a1 1 0 11-2 0V6.414l-3.293 3.293a1 1 0 01-1.414-1.414l5-5z"></path>
          </svg>
        </a>
      </div>

      <div class="p-6 border border-gray-600 hover:bg-gray-900 transition rounded-lg">
        <h2 class="text-lg font-semibold mb-4">02 DEVELOPMENT</h2>
        <p class="text-gray-400 mb-6">Get custom web development solutions tailored to your specifications, designed to deliver a flawless user experience.</p>
        <a href="#" class="flex items-center text-sm text-gray-300 hover:text-white">
          ABOUT WEBFLOW
          <svg class="ml-2 w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
            <path d="M12.293 3.293a1 1 0 011.414 0l5 5a1 1 0 01-1.414 1.414L14 6.414V17a1 1 0 11-2 0V6.414l-3.293 3.293a1 1 0 01-1.414-1.414l5-5z"></path>
          </svg>
        </a>
      </div>

      <div class="p-6 border border-gray-600 hover:bg-gray-900 transition rounded-lg">
        <h2 class="text-lg font-semibold mb-4">03 CONTENT & SEO</h2>
        <p class="text-gray-400 mb-6">Proven SEO strategies that enhance your online performance, bringing you to the forefront of organic search results.</p>
        <a href="#" class="flex items-center text-sm text-gray-300 hover:text-white">
          ABOUT SEO
          <svg class="ml-2 w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
            <path d="M12.293 3.293a1 1 0 011.414 0l5 5a1 1 0 01-1.414 1.414L14 6.414V17a1 1 0 11-2 0V6.414l-3.293 3.293a1 1 0 01-1.414-1.414l5-5z"></path>
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ServicesGrid',
};
</script>
