<template>
  <section class="py-24 px-6 bg-black text-gray-100 flex flex-col items-center opacity-0 transform translate-y-10" ref="contactFormSection">
    <div class="text-center mb-12">
      <h2 class="text-5xl font-light italic">Get in Touch</h2>
      <p class="text-lg font-light text-gray-300">
        Have a question or want to work together? Send us a message!
      </p>
    </div>

    <form
      class="bg-gray-700 bg-opacity-50 shadow-md rounded-lg px-8 py-6 w-full max-w-lg backdrop-filter backdrop-blur-md"
      @submit.prevent="sendMessage"
    >
      <div class="mb-4">
        <label
          for="name"
          class="block text-gray-300 text-sm font-bold mb-2"
        >
          Name
        </label>
        <input
          type="text"
          id="name"
          v-model="form.name"
          placeholder="Your Name"
          class="animated-placeholder appearance-none border border-gray-500 rounded w-full py-2 px-3 text-gray-300 bg-gray-800 leading-tight focus:outline-none focus:ring-2 focus:ring-gray-500"
        />
      </div>

      <div class="mb-4">
        <label
          for="email"
          class="block text-gray-300 text-sm font-bold mb-2"
        >
          Email
        </label>
        <input
          type="email"
          id="email"
          v-model="form.email"
          placeholder="Your Email"
          class="animated-placeholder appearance-none border border-gray-500 rounded w-full py-2 px-3 text-gray-300 bg-gray-800 leading-tight focus:outline-none focus:ring-2 focus:ring-gray-500"
        />
      </div>

      <div class="mb-6">
        <label
          for="message"
          class="block text-gray-300 text-sm font-bold mb-2"
        >
          Message
        </label>
        <textarea
          id="message"
          v-model="form.message"
          placeholder="Your Message"
          rows="4"
          class="animated-placeholder appearance-none border border-gray-500 rounded w-full py-2 px-3 text-gray-300 bg-gray-800 leading-tight focus:outline-none focus:ring-2 focus:ring-gray-500"
        ></textarea>
      </div>

      <div class="flex items-center justify-center">
        <button
          type="submit"
          class="bg-gray-600 bg-opacity-75 text-gray-100 px-6 py-3 rounded-lg hover:bg-gray-500 transition duration-300"
        >
          Send Message
        </button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  name: "ContactForm",
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    async sendMessage() {
      const webhookUrl =
        "https://discord.com/api/webhooks/1306877982010511380/nNpGGTi7S4mt1c5xg0AvY1xd4Xmy9ITWFdeUkeShop9taC2dopQ11DQJ4khX9yZl3dV0";
      const payload = {
        content: `**Name:** ${this.form.name}\n**Email:** ${this.form.email}\n**Message:** ${this.form.message}`,
      };

      try {
        const response = await fetch(webhookUrl, {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify(payload),
        });

        if (response.ok) {
          alert("Message sent successfully!");
          this.form.name = "";
          this.form.email = "";
          this.form.message = "";
        } else {
          alert("Failed to send message.");
        }
      } catch (error) {
        alert("An error occurred. Please try again later.");
      }
    },
  },
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
    observer.observe(this.$refs.contactFormSection);
  },
};
</script>

<style scoped>
.animated-placeholder::placeholder {
  color: #4a5568;
  transition: color 0.3s ease-in-out;
}

.animated-placeholder:focus::placeholder {
  color: transparent;
}

form {
  background-color: rgba(55, 65, 81, 0.5); /* Transparent form background */
}

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
