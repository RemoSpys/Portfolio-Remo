<template>
  <section class="py-24 px-6 bg-black text-white text-center">
    <h2 class="text-4xl font-semibold mb-4">What my <span class="italic">clients say</span></h2>
    <p class="text-gray-400 mb-12">See what my clients have to say about working with me and the results I helped them achieve.</p>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback1">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="Anonymous avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Anonymous</h3>
            <p class="text-sm text-gray-400">Web Development</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Exceptional service! Delivered a fully functional and modern website tailored to my business needs.
        </p>
      </div>

      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback2">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="Anonymous avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Anonymous</h3>
            <p class="text-sm text-gray-400">FiveM Server Setup</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Built and customized our entire FiveM server from scratch. Highly professional and efficient service.
        </p>
      </div>

      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback3">
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

      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback4">
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

      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback5">
        <div class="flex items-center mb-4">
          <img src="@/assets/unknown.jpg" alt="Anonymous avatar" class="w-12 h-12 rounded-full mr-4">
          <div>
            <h3 class="font-semibold">Anonymous</h3>
            <p class="text-sm text-gray-400">Custom Scripts</p>
          </div>
        </div>
        <p class="text-left text-gray-300">
          Delivered high-quality custom scripts for our project. The attention to detail was impressive.
        </p>
      </div>

      <div class="bg-gray-800 p-6 rounded-lg shadow-lg flex flex-col items-start opacity-0 transform translate-y-10" ref="feedback6">
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
    </div>
  </section>
</template>

<script>
export default {
  name: 'ClientFeedback',
  mounted() {
    const observerOptions = {
      threshold: 0.1,
    };

    const callback = (entries) => {
      entries.forEach((entry, index) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            entry.target.classList.add('fade-in');
          }, index * 200);
          observer.unobserve(entry.target);
        }
      });
    };

    const observer = new IntersectionObserver(callback, observerOptions);

    [
      this.$refs.feedback1,
      this.$refs.feedback2,
      this.$refs.feedback3,
      this.$refs.feedback4,
      this.$refs.feedback5,
      this.$refs.feedback6,
    ].forEach((el) => {
      observer.observe(el);
    });
  },
};
</script>

<style scoped>
@keyframes fade-in-up {
  0% {
    opacity: 0;
    transform: translateY(10px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.fade-in {
  animation: fade-in-up 0.8s ease-in-out forwards;
}

.opacity-0 {
  opacity: 0;
}

.transform {
  transform: translateY(10px);
}
</style>
