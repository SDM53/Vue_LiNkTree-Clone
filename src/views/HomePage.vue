<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Sergio D. Morfin',
  slogan: 'Dealing with stuff one day at a time...',
  avatar:
    'https://image2url.com/r2/default/images/1771214454336-60871f05-b319-41e5-8c26-740113ccee98.webp',
  links: [
    {
      id: 1,
      title: 'GitHub',
      url: 'https://github.com/SDM53?tab=repositories',
      description: 'Check out my projects on GitHub!',
    },
    {
      id: 2,
      title: 'Youtube',
      url: 'https://www.youtube.com/watch?v=tAe24CS-NCY&t=1s',
      description: 'Check out how this was made on YouTube!',
    },
  ],
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header-->
    <div class="mb-8 flex flex-col items-center">
      <div
        class="mb-4 h-48 w-48 overflow-hidden rounded-full border-4 border-blue-200 shadow-lg shadow-blue-400/90"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-blue-200 sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w -xs font text-blue-50 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
        :title="link.title"
        :url="link.url"
        :description="link.description"
      />
    </div>

    <!-- Nav Info -->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-blue-50 underline-offset-4 transition-colors duration-75 hover:text-blue-600 hover:underline"
      >About Me ➡️</RouterLink
    >
  </main>
</template>
