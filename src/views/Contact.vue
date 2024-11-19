<template>
  <section
    class="py-24 px-6 bg-gradient-to-b from-gray-900 to-gray-800 text-gray-100 flex flex-col items-center"
  >
    <div class="text-center mb-12">
      <!-- Profile Image -->
      <img
        src="/src/assets/profilepicture.webp"
        alt="Profile Picture"
        class="w-24 h-24 rounded-full mx-auto mb-6"
      />

      <!-- Get in Touch Header -->
      <h2
        class="text-5xl font-light italic text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700"
      >
        Get in Touch
      </h2>
      <p class="text-lg font-light text-gray-300">
        Have a question or want to work together? Send us a message!
      </p>
    </div>

    <form
      class="bg-gray-700 bg-opacity-50 shadow-md rounded-lg px-8 py-6 w-full max-w-lg backdrop-filter backdrop-blur-md"
      @submit.prevent="sendMessage"
    >
      <div class="mb-4">
        <label for="name" class="block text-gray-300 text-sm font-bold mb-2">
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
        <label for="email" class="block text-gray-300 text-sm font-bold mb-2">
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
        <label for="message" class="block text-gray-300 text-sm font-bold mb-2">
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
          class="bg-gradient-to-r from-blue-700 via-blue-800 to-blue-900 text-white font-light px-6 py-3 rounded-lg transition duration-300 ease-in-out transform hover:scale-105 hover:from-blue-800 hover:to-blue-900"
        >
          Send Message
        </button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: '',
      },
    }
  },
  methods: {
    async sendMessage() {
      const webhookUrl =
        'https://discord.com/api/webhooks/1306877982010511380/nNpGGTi7S4mt1c5xg0AvY1xd4Xmy9ITWFdeUkeShop9taC2dopQ11DQJ4khX9yZl3dV0'
      const payload = {
        content: `**Name:** ${this.form.name}\n**Email:** ${this.form.email}\n**Message:** ${this.form.message}`,
      }

      try {
        const response = await fetch(webhookUrl, {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
          },
          body: JSON.stringify(payload),
        })

        if (response.ok) {
          alert('Message sent successfully!')
          this.form.name = ''
          this.form.email = ''
          this.form.message = ''
        } else {
          alert('Failed to send message.')
        }
      } catch (error) {
        alert('An error occurred. Please try again later.')
      }
    },
  },
}
</script>

<style scoped>
/* Form background and other design elements */
form {
  background-color: rgba(55, 65, 81, 0.5); /* Transparent form background */
}

/* Styling for form inputs */
input,
textarea {
  background-color: #2d3748; /* Match with the page's background */
  color: #e2e8f0;
  border: 1px solid #4a5568;
  transition: border 0.3s;
}

/* Focus ring for form fields */
input:focus,
textarea:focus {
  border-color: #63b3ed;
  outline: none;
}

/* Styling the profile image */
img {
  border-radius: 50%;
  max-width: 120px;
  max-height: 120px;
  margin-bottom: 20px;
}

/* Styling for form labels */
label {
  color: #e2e8f0;
}

/* Gradient for header text */
h2 {
  background: linear-gradient(to right, #3b82f6, #2563eb);
  -webkit-background-clip: text;
  color: transparent;
}

h3 {
  font-size: 1.5rem;
  color: #3b82f6;
  font-weight: bold;
}
</style>
