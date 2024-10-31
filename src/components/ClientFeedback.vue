<template>
  <section class="py-24 px-6 bg-black text-white text-center">
    <h2 class="text-4xl font-semibold mb-4">What my <span class="italic">clients say</span></h2>
    <p class="text-gray-400 mb-12">See what my clients have to say about working with me and the results I helped them achieve.</p>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
      <!-- Client 1 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">John Smith</h3>
            <p class="text-sm text-gray-400">ABC Company</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Amazing results with the premium web design services. Attentive and provided excellent customer support.
        </p>
      </div>

      <!-- Client 2 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Karen Lee</h3>
            <p class="text-sm text-gray-400">TechSolutions</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Collaborative experience with a seamless process. Exceeded our expectations for web design.
        </p>
      </div>

      <!-- Client 3 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Emily Davis</h3>
            <p class="text-sm text-gray-400">Marketing Insights</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          SEO services boosted our online presence significantly. Highly recommend for all SEO needs.
        </p>
      </div>

      <!-- Client 4 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Michael Brown</h3>
            <p class="text-sm text-gray-400">Creative Solutions</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Professional web design that gave our brand a modern look. Delighted with the end result!
        </p>
      </div>

      <!-- Client 5 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Sophia Wilson</h3>
            <p class="text-sm text-gray-400">Startup Hub</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Incredible job on our website’s backend functionality. Highly recommended for development needs.
        </p>
      </div>

      <!-- Client 6 -->
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="User avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Liam Miller</h3>
            <p class="text-sm text-gray-400">Global Reach</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Seamless integration and excellent design. Thank you for bringing our ideas to life.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ClientFeedback',
};
</script>

<style scoped>
/* Optional custom styles */
</style>
