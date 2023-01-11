<template>
    <div class="flex flex-wrap w-1/3">
      <div class="w-full p-1 md:p-2">
        <NuxtImg
          class="block object-cover object-center w-full h-full rounded-lg"
          :alt="alt"
          format="webp"
          :src="src" />
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  const props = defineProps({
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    }
  })
  </script>