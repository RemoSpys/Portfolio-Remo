<template>
  <section class="relative">
    <!-- Hero Section with Navbar -->
    <div class="flex flex-col h-screen bg-[url('./src/assets/homebg.gif')] bg-cover bg-center">
      <Navbar />
      <div class="flex flex-row justify-center items-center flex-grow">
        <h1 class="glitch-text text-6xl md:text-9xl text-center mb-6 font-bold">
          Web Designer <br>& Developer
        </h1>
      </div>
    </div>

    <!-- About Section -->
    <div class="bg-black">
      <HomeAbout />
    </div>

    <!-- Services Section -->
    <div class="bg-black">
      <ServicesGrid />
    </div>

    <!-- Selected Work Section -->
    <div class="bg-black">
      <SelectedWorkGrid />
    </div>

    <!-- Client Feedback Section -->
    <div class="bg-black">
      <ClientFeedback />
    </div>

    <!-- Call-to-Action Section -->
    <div class="bg-yellow-200 text-gray-900">
      <LetsTalk />
    </div>

    <!-- Footer Section -->
    <Footer />
  </section>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import HomeAbout from '../components/HomeAbout.vue';
import ServicesGrid from '../components/ServicesGrid.vue';
import SelectedWorkGrid from '../components/SelectedWorkGrid.vue';
import ClientFeedback from '../components/ClientFeedback.vue';
import LetsTalk from '../components/LetsTalk.vue';
import Footer from '../components/Footer.vue';

export default {
  name: 'Home',
  components: {
    Navbar,
    HomeAbout,
    ServicesGrid,
    SelectedWorkGrid,
    ClientFeedback,
    LetsTalk,
    Footer
  }
};
</script>

<style scoped>
.glitch-text {
  position: relative;
  color: white;
  font-family: 'Nippo', sans-serif;
  animation: glitch 1s infinite alternate;
  text-shadow: 0px 0px 5px rgba(255, 255, 255, 0.8);
}

.glitch-text::before,
.glitch-text::after {
  content: 'Web Designer & Developer';
  position: absolute;
  left: 0;
  top: 0;
  color: white;
  background: transparent;
  overflow: hidden;
  clip: rect(0, 900px, 0, 0);
}

.glitch-text::before {
  left: 2px;
  text-shadow: -2px 0 red;
  animation: glitch-skew 1.5s infinite linear alternate-reverse;
}

.glitch-text::after {
  left: -2px;
  text-shadow: -2px 0 blue;
  animation: glitch-skew 1.5s infinite linear alternate;
}

@keyframes glitch {
  0% {
    transform: translate(0);
  }
  20% {
    transform: translate(-2px, -2px);
  }
  40% {
    transform: translate(2px, -2px);
  }
  60% {
    transform: translate(-2px, 2px);
  }
  80% {
    transform: translate(2px, 2px);
  }
  100% {
    transform: translate(0);
  }
}

@keyframes glitch-skew {
  0% {
    clip: rect(0, 900px, 0, 0);
  }
  10%, 50% {
    clip: rect(0, 900px, 100%, 0);
  }
  20%, 70% {
    clip: rect(0, 900px, 25%, 0);
  }
  30%, 90% {
    clip: rect(0, 900px, 75%, 0);
  }
  100% {
    clip: rect(0, 900px, 50%, 0);
  }
}
</style>
