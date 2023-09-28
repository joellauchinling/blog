<template>
  <main>
    <ContentDoc />
    <!-- <NuxtLink v-for="blog in blogs" :to="blog.path">{{ blog.title }}</NuxtLink> -->
    {{ blogs }}
  </main>
</template>

<script setup>
const { data: blogs } = await useAsyncData('blogs', () => queryContent('blog').find())
</script>