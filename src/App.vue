<template>
  <div class="flex flex-col min-h-screen">
    <Navbar v-if="!isHomeRoute" />
    <main class="flex-grow">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import { computed } from 'vue';
import { useRoute } from 'vue-router';

export default {
  components: {
    Navbar,
    Footer,
  },
  setup() {
    const route = useRoute();
    const isHomeRoute = computed(() => route.path === '/'); // Check the exact path

    return {
      isHomeRoute,
    };
  },
};
</script>
