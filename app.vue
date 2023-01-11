<template>
  <div>
    <CatImageGallery :images="images"/>
  </div>
</template>

<script setup lang="ts">
const client = useSupabaseClient()

const { data: images } = await useAsyncData('images', async () => client.from('images').select('*').order('created_at'), { transform: result => result.data })
</script>