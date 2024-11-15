<template>
  <section class="flex flex-col md:flex-row items-center justify-center text-white py-24 px-6 bg-black opacity-0 transform translate-y-10" ref="homeSection">
    <div class="text-center md:text-left md:w-1/3">
      <h1 class="text-5xl md:text-7xl font-bold italic typing-effect" ref="typingText">RemoSpys</h1>
      <p class="mt-4 text-2xl italic text-gray-300 typing-effect" ref="subTypingText">A website that leaves <br> <span class="text-xl">a lasting impression!</span></p>
    </div>

    <div class="w-full md:w-1/3 my-12 md:my-0 flex justify-center">
      <img src="@/assets/unknown.jpg" alt="RemoSpys" class="rounded-full w-80 h-80 object-cover shadow-lg">
    </div>

    <div class="text-center md:text-left md:w-1/3">
      <p class="text-gray-400 mb-6">
        Hi, I'm Remo – a freelancer specializing in premium web design, development, and SEO services.
        I'm passionate about creating unique and effective solutions for my clients, and I bring a personal touch to every project. Let's work together to bring your vision to life!
      </p>
      <div class="flex justify-center md:justify-start space-x-4 mt-4">
        <a href="#" class="hover:text-gray-400">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M22.46 6c-.77.35-1.6.59-2.46.7a4.3 4.3 0 001.88-2.37 8.54 8.54 0 01-2.72 1.04A4.28 4.28 0 0015.5 4c-2.42 0-4.38 1.97-4.38 4.39 0 .34.04.67.1.99C7.74 9.23 4.1 7.29 1.67 4.3a4.33 4.33 0 00-.6 2.21c0 1.52.77 2.86 1.94 3.64a4.27 4.27 0 01-1.99-.55v.06c0 2.12 1.5 3.89 3.49 4.3-.37.1-.76.15-1.15.15-.28 0-.55-.03-.82-.08.55 1.72 2.15 2.98 4.05 3.02a8.56 8.56 0 01-5.3 1.83c-.34 0-.68-.02-1.01-.07a12.1 12.1 0 006.58 1.93c7.88 0 12.2-6.54 12.2-12.21 0-.18 0-.35-.01-.52A8.68 8.68 0 0024 4.56a8.42 8.42 0 01-2.42.66A4.29 4.29 0 0022.46 6z"></path>
          </svg>
        </a>
        <a href="#" class="hover:text-gray-400">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2.2c2.99 0 3.38.01 4.58.06 1.18.05 1.9.24 2.35.41.57.22 1 .49 1.43.92.42.42.7.86.91 1.43.18.45.37 1.17.42 2.35.05 1.2.06 1.59.06 4.58s-.01 3.38-.06 4.58c-.05 1.18-.24 1.9-.41 2.35-.22.57-.49 1-.92 1.43-.42.42-.86.7-1.43.91-.45.18-1.17.37-2.35.42-1.2.05-1.59.06-4.58.06s-3.38-.01-4.58-.06c-1.18-.05-1.9-.24-2.35-.41-.57-.22-1-.49-1.43-.92-.42-.42-.7-.86-.91-1.43-.18-.45-.37-1.17-.42-2.35-.05-1.2-.06-1.59-.06-4.58s.01-3.38.06-4.58c.05-1.18.24-1.9.41-2.35.22-.57.49-1 .92-1.43.42-.42.86-.7 1.43-.91.45-.18 1.17-.37 2.35-.42C8.62 2.21 9.01 2.2 12 2.2zm0-2.2C8.74 0 8.28.01 7.05.06 5.83.1 4.94.24 4.13.53a4.8 4.8 0 00-1.78 1.18A4.8 4.8 0 001.18 4.1c-.29.8-.43 1.69-.47 3.05C.66 8.72.65 9.18.65 12c0 2.82.01 3.28.06 4.51.05 1.36.18 2.25.47 3.05.29.8.7 1.41 1.18 1.88a4.8 4.8 0 001.88 1.18c.8.29 1.69.43 3.05.47 1.23.05 1.69.06 4.51.06s3.28-.01 4.51-.06c1.36-.05 2.25-.18 3.05-.47a4.8 4.8 0 001.88-1.18 4.8 4.8 0 001.18-1.88c.29-.8.43-1.69.47-3.05.05-1.23.06-1.69.06-4.51s-.01-3.28-.06-4.51c-.05-1.36-.18-2.25-.47-3.05a4.8 4.8 0 00-1.18-1.88 4.8 4.8 0 00-1.88-1.18C16.72.66 15.83.52 14.47.47 13.28.42 12.82.4 12 .4h-.01z"></path>
          </svg>
        </a>
        <a href="#" class="hover:text-gray-400">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 0C5.372 0 0 5.373 0 12s5.372 12 12 12 12-5.373 12-12S18.627 0 12 0zm0 22.004c-5.524 0-10.004-4.481-10.004-10.004C1.996 6.478 6.477 2 12 2s10.004 4.478 10.004 10.004c0 5.522-4.48 10.003-10.004 10.003zm-1.507-7.712h1.225v6.7H10.5zm.612-3.792a1.125 1.125 0 01-1.129-1.13c0-.628.502-1.127 1.13-1.127s1.129.5 1.129 1.128a1.13 1.13 0 01-1.13 1.128z"></path>
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeAbout',
  mounted() {
    const observerOptions = {
      threshold: 0.1,
    };

    const fadeInCallback = (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
          observer.unobserve(entry.target);
        }
      });
    };

    const typingEffectCallback = (element, text) => {
      let index = 0;
      const interval = setInterval(() => {
        if (index < text.length) {
          element.textContent += text.charAt(index);
          index++;
        } else {
          clearInterval(interval);
        }
      }, 100);
    };

    const observer = new IntersectionObserver(fadeInCallback, observerOptions);
    observer.observe(this.$refs.homeSection);

    const typingTextElement = this.$refs.typingText;
    const subTypingTextElement = this.$refs.subTypingText;

    typingEffectCallback(typingTextElement, 'RemoSpys');
    typingEffectCallback(subTypingTextElement, 'A website that leaves a lasting impression!');
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
