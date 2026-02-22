<script setup>
import { ref } from 'vue'

const bio = ref({
  name: 'Sergio D. Morfin',
  avatar:
    'https://image2url.com/r2/default/images/1771214454336-60871f05-b319-41e5-8c26-740113ccee98.webp',
  about:
    'Just a guy taking a coding class this semester at STC...also adding some more random info/text cause I want to make this a little longer. But, I do not really want to add anything personal so this is what you get...:)',
  skills: [
    'Vue.js',
    'JavaScript',
    'HTML',
    'CSS',
    'Excel',
    'Photoshop',
    'InDesign',
    'Illustrator',
    'Java',
    'C++',
  ],
  email: 'smorfin@stu.southtexascollege.edu',
  location: 'McAllen, TX',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
    <RouterLink
      to="/"
      class="my-8 self-start text-sm text-blue-50 underline-offset-4 transition-colors duration-75 hover:text-blue-600 hover:underline"
      >⬅️ Go Back!
    </RouterLink>

    <!-- Profile Card -->
    <div
      class="w-full max-w-lg rounded-2xl border-6 border-purple-500 bg-purple-300 p-6 shadow-xl shadow-red-400/50 sm:p-8"
    >
      <!-- Header -->
      <div class="flex-column mb-6 flex items-center text-center sm:flex-row sm:text-left">
        <div
          class="mb-4 h-50 w-70 shrink-0 overflow-hidden rounded-full border-4 border-purple-500 shadow-xl shadow-yellow-400/50 sm:mr-6 sm:mb-0"
        >
          <img
            :src="bio.avatar"
            :alt="bio.name"
            class="h-full w-full object-cover"
          />
        </div>
        <div>
          <h1 class="mb-1 font-display text-2xl font-bold text-purple-700">{{ bio.name }}</h1>
          <p class="text-sm text-purple-500">🌎 {{ bio.location }}</p>
        </div>
      </div>

      <!-- About -->
      <div class="mb-6">
        <h2 class="mb-2 text-xl font-semibold text-purple-700">About</h2>
        <p class="leading-relaxed text-purple-600">{{ bio.about }}</p>
      </div>

      <!-- Skills -->
      <div class="mb-6">
        <h2 class="mb-2 text-xl font-semibold text-purple-700">Skills</h2>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in bio.skills"
            :key="skill"
            class="rounded-full bg-yellow-50 px-3 py-1 text-sm text-yellow-600"
            >{{ skill }}</span
          >
        </div>
      </div>

      <!-- Contact -->
      <div>
        <h2 class="mb-2 text-xl font-semibold text-purple-700">Get in Touch...</h2>
        <a
          :href="`mailto:${bio.email}`"
          class="group inline-flex items-center gap-2 rounded-full bg-red-300 px-8 py-3 font-medium text-red-900 shadow-lg shadow-yellow-200/30 transition-all duration-200 hover:scale-110 hover:bg-red-700 hover:text-red-100 hover:shadow-xl hover:shadow-yellow-300/50"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="h-5 w-5 transition-transform duration-200 group-hover:rotate-15"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75"
            />
          </svg>

          DON'T MAIL ME...</a
        >
      </div>
    </div>
  </main>
</template>
