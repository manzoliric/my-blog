<template>
  <div class="max-w-4xl mx-auto px-4 py-12">
    <h1 class="text-4xl font-bold mb-12 text-center">Blog</h1>
    
    <div class="space-y-8">
      <article v-for="post in blogPosts" :key="post.id" class="bg-gray-800 rounded-lg p-8 hover:bg-gray-700 transition-colors">
        <div class="flex items-center gap-4 mb-4">
          <span class="text-sm text-gray-400">{{ post.date }}</span>
          <span class="px-3 py-1 bg-gray-700 rounded-full text-sm">{{ post.category }}</span>
        </div>
        <h2 class="text-2xl font-semibold mb-4">{{ post.title }}</h2>
        <p class="text-gray-300 mb-4">{{ post.excerpt }}</p>
        <NuxtLink :to="`/blog/${post.slug}`" class="text-blue-400 hover:text-blue-300 font-medium">
          Ler mais →
        </NuxtLink>
      </article>
    </div>
  </div>
</template>

<script setup lang="ts">
const blogPosts = ref([
  {
    id: 1,
    slug: '---------------------------------',
    title: '---------------------------------',
    excerpt: '---------------------------------',
    date: '---------------------------------',
    category: '---------------------------------'
  },
])
</script> 