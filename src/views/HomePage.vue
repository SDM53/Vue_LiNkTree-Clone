<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Sergio D. Morfin',
  slogan: 'Dealing with stuff one day at a time...',
  avatar:
    'https://image2url.com/r2/default/images/1771214454336-60871f05-b319-41e5-8c26-740113ccee98.webp',
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
      <h1 class="mb-2 font-display text-2xl font-bold text-blue-200">{{ profile.name }}</h1>
      <p class="max-w -xs text-blue-50">{{ profile.slogan }}</p>
    </div>
  </main>
</template>
