<template>
  <div class="min-h-screen">
    <!-- Navigation Bar -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-gray-800/80 backdrop-blur-sm border-b border-gray-700">
      <div class="max-w-4xl mx-auto px-4 py-4">
        <div class="flex items-center justify-between">
          <div class="flex items-center space-x-8">
            <NuxtLink 
              to="/" 
              class="text-sm font-medium px-3 py-2 rounded-lg transition-colors"
              :class="$route.path === '/' ? 'bg-gray-700 text-white' : 'text-gray-300 hover:text-white hover:bg-gray-700'"
            >
              Início
            </NuxtLink>
            <NuxtLink 
              to="/blog" 
              class="text-sm font-medium px-3 py-2 rounded-lg transition-colors"
              :class="$route.path === '/blog' ? 'bg-gray-700 text-white' : 'text-gray-300 hover:text-white hover:bg-gray-700'"
            >
              Blog
            </NuxtLink>
            <NuxtLink 
              to="/about" 
              class="text-sm font-medium px-3 py-2 rounded-lg transition-colors"
              :class="$route.path === '/about' ? 'bg-gray-700 text-white' : 'text-gray-300 hover:text-white hover:bg-gray-700'"
            >
              Sobre
            </NuxtLink>
          </div>
          
        </div>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="pt-20">
      <NuxtPage />
    </main>
  </div>
</template>
