<template>
  <section class="py-24 px-6 bg-black text-white flex flex-col items-center opacity-0 transform translate-y-10" ref="workSection">
    <h2 class="text-4xl font-semibold mb-12">Selected <span class="italic">Work</span></h2>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div class="relative w-full max-w-xs md:max-w-md rounded-lg overflow-hidden flex flex-col items-center" style="width: 100%; max-width: 16cm; height: 16cm;">
        <div class="w-full h-full rounded-lg overflow-hidden flex items-center justify-center group">
          <img src="@/assets/work1.png" alt="Work 1" class="w-full h-full object-cover rounded-lg transform group-hover:scale-105 transition duration-300 ease-in-out">
          <div class="bg-black bg-opacity-60 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300 ease-in-out w-full h-full absolute rounded-lg">
            <span class="text-white text-lg font-semibold bg-white bg-opacity-20 py-2 px-4 rounded-lg">Explore Space</span>
          </div>
        </div>
      </div>

      <div class="relative w-full max-w-xs md:max-w-md rounded-lg overflow-hidden flex flex-col items-center" style="width: 100%; max-width: 16cm; height: 16cm;">
        <div class="w-full h-full rounded-lg overflow-hidden flex items-center justify-center group">
          <img src="@/assets/work2.png" alt="Work 2" class="w-full h-full object-cover rounded-lg transform group-hover:scale-105 transition duration-300 ease-in-out">
          <div class="bg-black bg-opacity-60 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300 ease-in-out w-full h-full absolute rounded-lg">
            <span class="text-white text-lg font-semibold bg-white bg-opacity-20 py-2 px-4 rounded-lg">Discover Nova</span>
          </div>
        </div>
      </div>

      <div class="relative w-full max-w-xs md:max-w-md rounded-lg overflow-hidden flex flex-col items-center" style="width: 100%; max-width: 16cm; height: 16cm;">
        <div class="w-full h-full rounded-lg overflow-hidden flex items-center justify-center group">
          <img src="@/assets/work3.png" alt="Work 3" class="w-full h-full object-cover rounded-lg transform group-hover:scale-105 transition duration-300 ease-in-out">
          <div class="bg-black bg-opacity-60 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300 ease-in-out w-full h-full absolute rounded-lg">
            <span class="text-white text-lg font-semibold bg-white bg-opacity-20 py-2 px-4 rounded-lg">Explore Sonic</span>
          </div>
        </div>
      </div>

      <div class="relative w-full max-w-xs md:max-w-md rounded-lg overflow-hidden flex flex-col items-center" style="width: 100%; max-width: 16cm; height: 16cm;">
        <div class="w-full h-full rounded-lg overflow-hidden flex items-center justify-center group">
          <img src="@/assets/work4.png" alt="Work 4" class="w-full h-full object-cover rounded-lg transform group-hover:scale-105 transition duration-300 ease-in-out">
          <div class="bg-black bg-opacity-60 flex items-center justify-center opacity-0 group-hover:opacity-100 transition duration-300 ease-in-out w-full h-full absolute rounded-lg">
            <span class="text-white text-lg font-semibold bg-white bg-opacity-20 py-2 px-4 rounded-lg">Discover Solar</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SelectedWorkGrid',
  mounted() {
    const observerOptions = {
      threshold: 0.1,
    };

    const callback = (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
          observer.unobserve(entry.target);
        }
      });
    };

    const observer = new IntersectionObserver(callback, observerOptions);
    observer.observe(this.$refs.workSection);
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
