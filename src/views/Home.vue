<template>
  <section
    class="flex flex-col h-screen bg-[url(./src/assets/home.webp)] bg-cover bg-center"
  >
    <div class="flex flex-row justify-center items-center flex-grow">
      <h1 class="text-white text-6xl md:text-9xl text-center mb-6">
        <span
          id="typing-text"
          class="inline-block"
          style="font-family: 'Nippo', sans-serif"
        ></span>
      </h1>
    </div>

    <div class="flex justify-center pb-20 mt-10 animate-bounce">
      <!-- See More Button -->
      <div
        class="flex flex-col items-center text-white space-y-2 cursor-pointer"
        @click="smoothScroll"
        role="button"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          class="w-10 h-10"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M8 1.5a.5.5 0 0 1 .5.5v10.793l3.146-3.147a.5.5 0 0 1 .708.708l-4 4a.5.5 0 0 1-.708 0l-4-4a.5.5 0 0 1 .708-.708L7.5 12.793V2a.5.5 0 0 1 .5-.5z"
          />
        </svg>
        <span class="text-lg font-semibold">More</span>
      </div>
    </div>
  </section>
  <section
    id="skills"
    class="flex flex-col p-6 md:p-20 bg-gray-900 text-gray-300"
  >
    <div class="relative overflow-hidden">
      <div class="flex animate-marquee w-max">
        <div class="flex">
          <i
            v-for="skill in skills"
            :key="skill"
            :class="[
              `devicon-${skill}-plain`,
              'text-6xl md:text-8xl text-gray-400',
              'mx-8',
            ]"
          ></i>
        </div>
        <div class="flex">
          <i
            v-for="skill in skills"
            :key="'repeat-' + skill"
            :class="[
              `devicon-${skill}-plain`,
              'text-6xl md:text-8xl text-gray-400',
              'mx-8',
            ]"
          ></i>
        </div>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section
    class="flex flex-col md:flex-row space-y-6 md:space-y-0 md:space-x-6 px-6 md:px-12 py-10 bg-gray-900 text-gray-300"
  >
    <!-- Service Card 1: Web Design Magic -->
    <div
      ref="serviceCard1"
      class="service-card opacity-0 transition-opacity duration-1000 bg-gray-800 p-6 rounded-lg border-2 border-gray-700 shadow-lg"
      :class="{ 'service-card-visible': isServiceCard1Visible }"
    >
      <p
        class="text-3xl font-bold text-gradient-from-cyan"
        style="font-family: 'Nippo', sans-serif"
      >
        01
      </p>
      <h2 class="text-2xl font-semibold text-gray-100 mt-2">
        Web Design Magic
      </h2>
      <p class="mt-4 text-gray-400">
        Turning Your Dreams into Digital Realities! Let’s bring your ideas to
        life with stunning, creative, and vibrant web designs that capture your
        brand and engage your audience.
      </p>
      <div class="flex items-center mt-6">
        <router-link
          to="/services#web-design"
          class="bg-gradient-to-r from-cyan-400 to-cyan-600 text-white px-5 py-2 rounded-lg hover:bg-gradient-to-r hover:from-blue-800 hover:to-blue-900 transition ease-in-out duration-300"
        >
          About Web Design Magic
        </router-link>
      </div>
    </div>

    <!-- Service Card 2: Development -->
    <div
      ref="serviceCard2"
      class="service-card opacity-0 transition-opacity duration-1000 bg-gray-800 p-6 rounded-lg border-2 border-gray-700 shadow-lg"
      :class="{ 'service-card-visible': isServiceCard2Visible }"
    >
      <p
        class="text-3xl font-bold text-gradient-from-cyan"
        style="font-family: 'Nippo', sans-serif"
      >
        02
      </p>
      <h2 class="text-2xl font-semibold text-gray-100 mt-2">Development</h2>
      <p class="mt-4 text-gray-400">
        High-Performance, Clean, and Animated Websites. Get fast, smooth, and
        optimized websites built to perform flawlessly across all devices, with
        interactive animations and user-friendly design.
      </p>
      <div class="flex items-center mt-6">
        <router-link
          to="/services#development"
          class="bg-gradient-to-r from-cyan-400 to-cyan-600 text-white px-5 py-2 rounded-lg hover:bg-gradient-to-r hover:from-blue-800 hover:to-blue-900 transition ease-in-out duration-300"
        >
          About Development
        </router-link>
      </div>
    </div>

    <!-- Service Card 3: Web Design Mastery -->
    <div
      ref="serviceCard3"
      class="service-card opacity-0 transition-opacity duration-1000 bg-gray-800 p-6 rounded-lg border-2 border-gray-700 shadow-lg"
      :class="{ 'service-card-visible': isServiceCard3Visible }"
    >
      <p
        class="text-3xl font-bold text-gradient-from-cyan"
        style="font-family: 'Nippo', sans-serif"
      >
        03
      </p>
      <h2 class="text-2xl font-semibold text-gray-100 mt-2">
        Web Design Mastery
      </h2>
      <p class="mt-4 text-gray-400">
        Bringing Your Vision to Life Digitally. From tailored web concepts to
        seamless FiveM server customizations, we design solutions that perfectly
        match your brand's identity and audience needs.
      </p>
      <div class="flex items-center mt-6">
        <router-link
          to="/services#web-design-mastery"
          class="bg-gradient-to-r from-cyan-400 to-cyan-600 text-white px-5 py-2 rounded-lg hover:bg-gradient-to-r hover:from-blue-800 hover:to-blue-900 transition ease-in-out duration-300"
        >
          About Web Design Mastery
        </router-link>
      </div>
    </div>
  </section>

  <section class="flex flex-col items-center p-10 text-gray-300 bg-gray-900">
    <div class="text-center">
      <p class="font-semibold uppercase tracking-wide text-gray-400">
        The Process
      </p>
      <h1 class="text-4xl md:text-6xl pb-4 text-gray-100">
        Your Website <br />
        <span
          style="font-family: 'Nippo', sans-serif"
          class="italic bg-gradient-to-r from-gray-500 via-gray-600 to-gray-500 text-transparent bg-clip-text"
        >
          in 5 Steps
        </span>
      </h1>
      <p class="font-medium text-gray-400">
        Our process ensures we create a website <br class="hidden md:block" />
        tailored to your business needs.
      </p>
    </div>
  </section>

  <section class="relative px-6 md:px-20 pb-8 bg-gray-900 text-gray-300">
    <div
      class="relative space-y-16 before:absolute before:inset-0 before:mx-auto before:w-0.5 before:bg-gradient-to-b from-gray-600 via-gray-700 to-gray-800"
    >
      <!-- Step 1 -->
      <div
        ref="step1"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isStep1Visible }"
      >
        <div class="relative md:flex md:items-start md:space-x-8">
          <div class="flex justify-center md:ml-19 md:justify-end md:w-1/2">
            <div
              class="relative flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-r from-cyan-500 to-cyan-700 text-white shadow"
            >
              1
            </div>
          </div>
          <div class="relative w-full md:w-1/2 mt-6 md:mt-0 md:pl-10">
            <div
              class="p-6 border border-gray-700 rounded-2xl shadow-lg bg-gray-800 hover:shadow-2xl transition duration-300 transform hover:-translate-y-1"
            >
              <p
                class="uppercase tracking-widest text-xs font-semibold text-gray-400 mb-3"
              >
                Let's Make It Happen
              </p>
              <h2 class="text-3xl font-extrabold mb-4 text-gray-100">
                Initial Consultation
              </h2>
              <p class="mb-6 text-gray-400 font-medium leading-relaxed">
                The first step is to get to know your business. We discuss your
                goals, challenges, and the direction you want to go in.
              </p>
              <ul class="space-y-3 text-gray-400">
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Understanding your vision</span>
                </li>
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Assessing the project scope</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Step 2 -->
      <div
        ref="step2"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isStep2Visible }"
      >
        <div
          class="relative md:flex md:items-start md:space-x-8 md:flex-row-reverse"
        >
          <div class="flex justify-center md:mr-19 md:justify-start md:w-1/2">
            <div
              class="relative flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-r from-cyan-500 to-cyan-700 text-white shadow"
            >
              2
            </div>
          </div>
          <div class="relative w-full md:w-1/2 mt-6 md:mt-0 md:pr-10">
            <div
              class="p-6 border border-gray-700 rounded-2xl shadow-lg bg-gray-800 hover:shadow-2xl transition duration-300 transform hover:-translate-y-1"
            >
              <p
                class="uppercase tracking-widest text-xs font-semibold text-gray-400 mb-3"
              >
                Strategizing Your Success
              </p>
              <h2 class="text-3xl font-extrabold mb-4 text-gray-100">
                Plan & Prototype
              </h2>
              <p class="mb-6 text-gray-400 font-medium leading-relaxed">
                Based on your objectives, we create wireframes, mockups, and
                interactive prototypes to showcase your digital experience.
              </p>
              <ul class="space-y-3 text-gray-400">
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Building the initial structure</span>
                </li>
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Defining the user journey</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Step 3 -->
      <div
        ref="step3"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isStep3Visible }"
      >
        <div class="relative md:flex md:items-start md:space-x-8">
          <div class="flex justify-center md:ml-19 md:justify-end md:w-1/2">
            <div
              class="relative flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-r from-cyan-500 to-cyan-700 text-white shadow"
            >
              3
            </div>
          </div>
          <div class="relative w-full md:w-1/2 mt-6 md:mt-0 md:pl-10">
            <div
              class="p-6 border border-gray-700 rounded-2xl shadow-lg bg-gray-800 hover:shadow-2xl transition duration-300 transform hover:-translate-y-1"
            >
              <p
                class="uppercase tracking-widest text-xs font-semibold text-gray-400 mb-3"
              >
                Bringing It to Life
              </p>
              <h2 class="text-3xl font-extrabold mb-4 text-gray-100">
                Developing Your Solution
              </h2>
              <p class="mb-6 text-gray-400 font-medium leading-relaxed">
                Now it's time to code. We develop a fully responsive,
                high-performance website or application that works across
                devices and browsers.
              </p>
              <ul class="space-y-3 text-gray-400">
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Responsive design for all devices</span>
                </li>
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Optimized for performance</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Step 4 -->
      <div
        ref="step4"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isStep4Visible }"
      >
        <div
          class="relative md:flex md:items-start md:space-x-8 md:flex-row-reverse"
        >
          <div class="flex justify-center md:mr-19 md:justify-start md:w-1/2">
            <div
              class="relative flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-r from-cyan-500 to-cyan-700 text-white shadow"
            >
              4
            </div>
          </div>
          <div class="relative w-full md:w-1/2 mt-6 md:mt-0 md:pr-10">
            <div
              class="p-6 border border-gray-700 rounded-2xl shadow-lg bg-gray-800 hover:shadow-2xl transition duration-300 transform hover:-translate-y-1"
            >
              <p
                class="uppercase tracking-widest text-xs font-semibold text-gray-400 mb-3"
              >
                Testing & QA
              </p>
              <h2 class="text-3xl font-extrabold mb-4 text-gray-100">
                Quality Assurance
              </h2>
              <p class="mb-6 text-gray-400 font-medium leading-relaxed">
                We perform thorough testing to ensure everything is bug-free,
                functional, and optimized for speed.
              </p>
              <ul class="space-y-3 text-gray-400">
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Testing for all devices</span>
                </li>
                <li class="flex items-start">
                  <span
                    class="flex-shrink-0 w-4 h-4 bg-gradient-to-r from-gray-600 to-gray-700 rounded-full mr-3 mt-1"
                  ></span>
                  <span>Cross-browser compatibility</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Step 5 -->
      <div
        ref="step5"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isStep5Visible }"
      >
        <div class="relative md:flex md:items-start md:space-x-8">
          <div class="flex justify-center md:ml-19 md:justify-end md:w-1/2">
            <div
              class="relative flex items-center justify-center w-10 h-10 rounded-full bg-gradient-to-r from-cyan-500 to-cyan-700 text-white shadow"
            >
              5
            </div>
          </div>
          <div class="relative w-full md:w-1/2 mt-6 md:mt-0 md:pl-10">
            <div
              class="p-6 border border-gray-700 rounded-2xl shadow-lg bg-gray-800 hover:shadow-2xl transition duration-300 transform hover:-translate-y-1"
            >
              <p
                class="uppercase tracking-widest text-xs font-semibold text-gray-400 mb-3"
              >
                Launch
              </p>
              <h2 class="text-3xl font-extrabold mb-4 text-gray-100">
                Go Live & Ongoing Support
              </h2>
              <p class="mb-6 text-gray-400 font-medium leading-relaxed">
                Once everything is ready, we launch your website and continue to
                support you with updates and optimization.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="py-8 px-4 bg-gray-900 text-gray-300">
    <!-- Header Section -->
    <div
      ref="testimonialsHeader"
      class="text-center mb-8 opacity-0 transition-opacity duration-1000"
      :class="{ 'opacity-100': isTestimonialsHeaderVisible }"
    >
      <h1 class="text-4xl md:text-6xl lg:text-7xl pb-4 text-gray-100">
        What My <br />
        <span
          style="font-family: 'Nippo', sans-serif"
          class="italic bg-gradient-to-r from-gray-400 via-gray-500 to-gray-400 text-transparent bg-clip-text"
        >
          Clients Say
        </span>
      </h1>
      <p class="font-medium text-gray-400 text-lg md:text-xl">
        See what my clients have to say about working with me and the
        <br class="hidden md:block" />
        results I helped them achieve.
      </p>
    </div>

    <!-- Testimonials Grid -->
    <div
      ref="testimonialsGrid"
      class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8 max-w-6xl mx-auto opacity-0 transition-opacity duration-1000"
      :class="{ 'opacity-100': isTestimonialsGridVisible }"
    >
      <!-- Testimonial Card 1 -->
      <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-lg">
        <h2 class="text-xl font-bold text-gray-100 mb-2">
          Outstanding Results with RemoSpy's Expertise.
        </h2>
        <p class="mt-4 leading-relaxed text-gray-400 italic">
          "RemoSpy created a stunning website for my business. Their attention
          to detail and customer focus were unmatched. Highly recommend them as
          the best website makers!"
        </p>

        <div class="flex items-center mt-6">
          <img
            src="/src/assets/unknown.jpg"
            class="h-16 w-16 rounded-full border-2 border-gray-600"
            alt="Client Image"
          />
          <div class="ml-4">
            <h3 class="uppercase tracking-wider font-semibold text-gray-200">
              Friend 1
            </h3>
            <p class="text-gray-400">CEO of School</p>
          </div>
        </div>
      </div>

      <!-- Testimonial Card 2 -->
      <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-lg">
        <h2 class="text-xl font-bold text-gray-100 mb-2">
          Transformative Web Design Experience.
        </h2>
        <p class="mt-4 leading-relaxed text-gray-400 italic">
          "The website designed by RemoSpy has elevated our brand's online
          presence. Their creativity, dedication, and performance-optimized
          scripts for FiveM are phenomenal! 10/10, I highly recommend them!"
        </p>

        <div class="flex items-center mt-6">
          <img
            src="/src/assets/unknown.jpg"
            class="h-16 w-16 rounded-full border-2 border-gray-600"
            alt="Client Image"
          />
          <div class="ml-4">
            <h3 class="uppercase tracking-wider font-semibold text-gray-200">
              Friend 2
            </h3>
            <p class="text-gray-400">Director of Roblox</p>
          </div>
        </div>
      </div>

      <!-- Testimonial Card 3 -->
      <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-lg">
        <h2 class="text-xl font-bold text-gray-100 mb-2">
          Transformative Web Design Experience.
        </h2>
        <p class="mt-4 leading-relaxed text-gray-400 italic">
          "The website RemoSpy designed has elevated our brand's online
          presence. Their creativity and dedication are phenomenal! With
          excellent performance scripts for FiveM, I highly recommend them —
          10/10!"
        </p>

        <div class="flex items-center mt-6">
          <img
            src="/src/assets/unknown.jpg"
            class="h-16 w-16 rounded-full border-2 border-gray-600"
            alt="Client Image"
          />
          <div class="ml-4">
            <h3 class="uppercase tracking-wider font-semibold text-gray-200">
              Friend 3
            </h3>
            <p class="text-gray-400">Developer</p>
          </div>
        </div>
      </div>

      <!-- Testimonial Card 4 -->
      <div class="bg-gray-800 p-6 rounded-lg border border-gray-700 shadow-lg">
        <h2 class="text-xl font-bold text-gray-100 mb-2">
          A Seamless Collaboration.
        </h2>
        <p class="mt-4 leading-relaxed text-gray-400 italic">
          "RemoSpy brought my vision to life with a website that exceeded my
          expectations. A true professional with exceptional talent! RemoSpy is
          the best dev, with fast support and the ability to do anything — no
          barriers!"
        </p>

        <div class="flex items-center mt-6">
          <img
            src="/src/assets/unknown.jpg"
            class="h-16 w-16 rounded-full border-2 border-gray-600"
            alt="Client Image"
          />
          <div class="ml-4">
            <h3 class="uppercase tracking-wider font-semibold text-gray-200">
              Friend 4
            </h3>
            <p class="text-gray-400">Owner of FiveM</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Mobile Menu -->
  <section>
    <!-- Profile Section -->
    <div class="relative bg-gray-900 text-gray-300 font-sans pb-8">
      <div
        ref="profileSection"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isProfileVisible }"
      >
        <div
          class="flex flex-col md:flex-row items-center justify-center px-6 py-20 md:py-32 gap-6"
        >
          <!-- Profile Image -->
          <div class="flex justify-center items-center">
            <img
              class="w-24 h-24 md:w-32 md:h-32 rounded-full"
              src="/src/assets/profilepicture.webp"
              alt="Profile Image"
            />
          </div>

          <!-- "Remo Spy's" Text -->
          <div
            class="text-4xl md:text-6xl font-serif text-center md:text-left bg-gradient-to-r from-gray-400 via-gray-500 to-gray-400 text-transparent bg-clip-text"
          >
            Remo
            <span class="italic">Spy's</span>
          </div>
        </div>

        <!-- Description Section -->
        <div class="max-w-7xl mx-auto mt-16 px-6 md:px-10">
          <div
            class="flex flex-col md:flex-row items-center md:items-end gap-8"
          >
            <!-- Left Column -->
            <div
              class="md:w-1/2 flex flex-col justify-center text-center md:text-right mb-6 md:mb-12 pr-0 md:pr-8 md:border-r-8 border-gray-600"
            >
              <h2 class="text-2xl md:text-3xl font-semibold text-gray-100">
                Create a
                <span
                  class="italic font-bold bg-gradient-to-r from-cyan-400 to-cyan-600 text-transparent bg-clip-text"
                >
                  lasting impression
                </span>

                with a stunning website!
              </h2>
              <p class="mt-4 text-gray-400 text-sm md:text-base">
                I design and build websites that tell your story, captivate your
                audience, and deliver measurable results.
              </p>
            </div>

            <!-- Right Column -->
            <div
              class="md:w-1/2 flex flex-col justify-center text-center md:text-left"
            >
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                Hi, I'm Remo – a freelancer specializing in premium web design
                and development. I'm passionate about creating unique and
                effective solutions for my clients, bringing a personal touch to
                every project.
              </p>
              <p
                class="mt-4 text-gray-400 text-sm md:text-base leading-relaxed"
              >
                Let's collaborate to craft a digital experience that stands out
                in a crowded marketplace.
              </p>

              <!-- Social Media Icons -->
              <div class="flex justify-center md:justify-start gap-6 mt-6">
                <a
                  href="https://www.facebook.com/"
                  class="text-gray-500 hover:text-blue-400 transition-transform transform hover:scale-110"
                >
                  <i class="fab fa-facebook fa-2x"></i>
                </a>
                <a
                  href="https://github.com/"
                  class="text-gray-500 hover:text-blue-400 transition-transform transform hover:scale-110"
                >
                  <i class="fab fa-github fa-2x"></i>
                </a>
                <a
                  href="https://www.linkedin.com/"
                  class="text-gray-500 hover:text-blue-400 transition-transform transform hover:scale-110"
                >
                  <i class="fab fa-linkedin fa-2x"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Call-to-Action Section -->
    <div
      class="text-gray-300 flex flex-col justify-between bg-gradient-to-b from-gray-900 to-gray-800"
    >
      <div
        ref="ctaSection"
        class="opacity-0 transition-opacity duration-1000"
        :class="{ 'opacity-100': isCTAVisible }"
      >
        <div class="text-center py-20 px-6">
          <p class="uppercase tracking-widest text-gray-400 text-xl">
            Let's Build Your Digital Future
          </p>
          <h1 class="text-4xl md:text-7xl font-semibold mt-4 text-slate-100">
          Ready to Start Your <br />
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-cyan-600 italic"
          >
            Website
          </span>
          or
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-cyan-600 italic"
          >
            Game Script
          </span>
          Journey?
        </h1>
          <p class="mt-6 text-xl text-slate-300 max-w-xl mx-auto pb-20">
          Premium web design, development, and game scripting services to help
          your business and projects stand out with creativity and innovation.
        </p>
          <a
            href="/contact"
            class="mt-8 px-8 py-4 bg-gradient-to-r from-cyan-400 to-cyan-600 hover:from-blue-800 hover:to-blue-950 text-white font-light rounded-lg shadow-lg transition-transform transform hover:scale-105"
          >
            Get In Touch
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      skills: [
        'javascript',
        'python',
        'tailwindcss',
        'mysql',
        'vuejs',
        'php',
        'git',
        'figma',
      ],
      isProfileVisible: false,
      isCTAVisible: false,
      isTestimonialsHeaderVisible: false,
      isTestimonialsGridVisible: false,

      isStep1Visible: false,
      isStep2Visible: false,
      isStep3Visible: false,
      isStep4Visible: false,
      isStep5Visible: false,

      isServiceCard1Visible: false,
      isServiceCard2Visible: false,
      isServiceCard3Visible: false,
    }
  },
  mounted() {
    this.observeSection(this.$refs.profileSection, 'isProfileVisible')
    this.observeSection(this.$refs.ctaSection, 'isCTAVisible')
    this.observeSection(
      this.$refs.testimonialsHeader,
      'isTestimonialsHeaderVisible',
    )
    this.observeSection(
      this.$refs.testimonialsGrid,
      'isTestimonialsGridVisible',
    )
    this.observeSection(this.$refs.step1, 'isStep1Visible')
    this.observeSection(this.$refs.step2, 'isStep2Visible')
    this.observeSection(this.$refs.step3, 'isStep3Visible')
    this.observeSection(this.$refs.step4, 'isStep4Visible')
    this.observeSection(this.$refs.step5, 'isStep5Visible')
   
    this.observeSection(this.$refs.serviceCard1, 'isServiceCard1Visible')
    this.observeSection(this.$refs.serviceCard2, 'isServiceCard2Visible')
    this.observeSection(this.$refs.serviceCard3, 'isServiceCard3Visible')
  },
  methods: {
    observeSection(element, visibilityState) {
      const observer = new IntersectionObserver(
        ([entry]) => {
          if (entry.isIntersecting) {
            this[visibilityState] = true
          } else {
            this[visibilityState] = false
          }
        },
        { threshold: 0.2 }, 
      )
      observer.observe(element)
    },
    smoothScroll(event) {
      event.preventDefault()

      const target = document.querySelector('#skills')

      target.scrollIntoView({
        behavior: 'smooth',
        block: 'start', 
      })
    },
  },
}
document.addEventListener('DOMContentLoaded', () => {
  const typingElement = document.getElementById('typing-text')
  const textArray = ['Web Designer', 'Developer', 'Game Developer']
  let currentText = ''
  let currentIndex = 0 
  let isDeleting = false 
  let typingSpeed = 150 
  let deletingSpeed = 75
  let pauseDuration = 1000 

  function typeText() {
    if (!isDeleting) {
      currentText = textArray[currentIndex].substring(0, currentText.length + 1)
      typingElement.innerHTML = currentText
      if (currentText === textArray[currentIndex]) {
        setTimeout(() => {
          isDeleting = true
          setTimeout(typeText, pauseDuration)
        }, pauseDuration)
      } else {
        setTimeout(typeText, typingSpeed)
      }
    } else {
      currentText = textArray[currentIndex].substring(0, currentText.length - 1)
      typingElement.innerHTML = currentText
      if (currentText === '') {
        isDeleting = false
        currentIndex = (currentIndex + 1) % textArray.length
        setTimeout(typeText, typingSpeed)
      } else {
        setTimeout(typeText, deletingSpeed)
      }
    }
  }

  typeText()
})
</script>

<style scoped>
@keyframes marquee {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-marquee {
  display: flex;
  animation: marquee 15s linear infinite;
  will-change: transform;
}

.typing-effect {
  white-space: nowrap;
  overflow: hidden;
  border-right: 2px solid #ffffff;
  animation: blink 0.7s steps(2) infinite;
}

@keyframes blink {
  0% {
    border-color: transparent;
  }
  50% {
    border-color: #ffffff;
  }
  100% {
    border-color: transparent;
  }
}

.opacity-0 {
  opacity: 0;
}
.opacity-100 {
  opacity: 1;
}

.transition-opacity {
  transition: opacity 1s ease-in-out;
}

.transition-opacity {
  transition: opacity 1s ease-in-out;
}

.step-transition {
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.step-visible {
  opacity: 1;
}

.service-card {
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.service-card-visible {
  opacity: 1;
  transition: opacity 1s ease-in-out;
}

.bg-gray-800:hover {
  transform: scale(1.02);
  transition: transform 0.3s ease;
}

a:hover {
  transform: scale(1.05);
  transition: transform 0.3s ease-in-out;
}
#typing-text {
  display: inline-block;
  white-space: nowrap;
  border-right: 2px solid #ffffff;
  animation: blink 0.7s step-end infinite;
}

@keyframes blink {
  0% {
    border-color: transparent;
  }
  50% {
    border-color: #ffffff;
  }
  100% {
    border-color: transparent;
  }
}
</style>
