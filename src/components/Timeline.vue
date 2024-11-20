<template>
  <section class="py-16 px-6 bg-black text-gray-300 flex flex-col items-center">
    <div class="w-full max-w-4xl relative">
      <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-gray-600 hidden md:block"></div>

      <div v-for="(item, index) in timelineData" :key="index" class="mb-12 flex items-center justify-center relative md:flex-row flex-col">
        <div :class="['timeline-item', index % 2 === 0 ? 'left' : 'right', 'md:relative', 'relative w-full']">
          <div class="bg-gray-800 p-6 rounded-lg shadow-md">
            <div class="flex justify-between items-center mb-4">
              <h3 class="text-xl font-semibold text-gray-200">{{ item.title }}</h3>
              <span class="text-xs bg-gray-700 text-gray-400 py-1 px-2 rounded">{{ item.duration }}</span>
            </div>
            <p class="text-gray-400 mb-4">{{ item.description }}</p>
            <ul class="list-disc list-inside text-gray-400">
              <li v-for="(point, idx) in item.points" :key="idx">{{ point }}</li>
            </ul>
          </div>
        </div>

        <div class="circle-indicator flex items-center justify-center w-10 h-10 rounded-full bg-gray-600 text-white font-semibold md:absolute md:left-1/2 md:transform md:-translate-x-1/2 md:top-0 mt-4 md:mt-0 hidden md:flex">
          {{ index + 1 }}
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Timeline',
  data() {
    return {
      timelineData: [
        {
          title: 'DISCOVERY CALL',
          duration: '2 HOURS',
          description: 'Before we start, we determine if and how I can help you. What are your requirements for your new website?',
          points: [
            'Get to know each other better',
            'Determine how I can best assist you',
            'Understand the goals you have for your website',
          ],
        },
        {
          title: 'CONCEPT & STRATEGY',
          duration: '1 WEEK',
          description: 'Together, we develop a strategy that successfully combines your goals with the needs of your target audience.',
          points: ['UX Design', 'Wireframes', 'Interactive Prototype'],
        },
        {
          title: 'WEB DESIGN',
          duration: '1 WEEK',
          description: 'Based on the previously developed concept, I create a high-end screen design perfectly tailored to your brand.',
          points: ['High-end web design tailored to your brand', 'Interactive prototype of the design'],
        },
        {
          title: 'DEVELOPMENT',
          duration: '2 WEEKS',
          description: 'In this step, we breathe life into your new high-end design with modular web design systems and CMS integration.',
          points: ['Custom Framer website', 'Modular web design systems', 'CMS integration'],
        },
        {
          title: 'WEBSITE ONBOARDING',
          duration: '2 HOURS',
          description: 'In a personal Framer workshop, I will show you how to make changes to your new website quickly and easily.',
          points: ['Personal workshop', 'Personalized video tutorials', 'Edit text and images directly on your website'],
        },
      ],
    };
  },
};
</script>

<style scoped>
.absolute.left-1\/2 {
  transform: translateX(-50%);
}
.h-full {
  height: 100%;
}
.w-1 {
  width: 1px;
}
.bg-gray-600 {
  background-color: #333;
}

.timeline-item {
  width: 45%;
  position: relative;
}
.left {
  align-self: flex-start;
  margin-right: auto;
  padding-right: 2rem;
}
.right {
  align-self: flex-end;
  margin-left: auto;
  padding-left: 2rem;
}

.circle-indicator {
  top: 50%;
  transform: translate(-50%, -50%);
}
.mt-4 {
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .timeline-item {
    width: 100%;
    padding-left: 0 !important;
    padding-right: 0 !important;
    margin-top: 0 !important;
  }
  .left, .right {
    align-self: center;
    padding-left: 0;
    padding-right: 0;
  }
  .circle-indicator {
    display: none;
  }
}
</style>
