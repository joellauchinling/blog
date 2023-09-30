<template>
  <main>
    <ContentDoc />
    <NuxtLink v-for="blog in blogs" :to="blog._path">{{ blog.title }}</NuxtLink>
  </main>
</template>

<script setup>
const { data: blogs } = await useAsyncData('blogs', () => queryContent('blog').find())
</script>