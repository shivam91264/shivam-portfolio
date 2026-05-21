<template>
  <nav class="fixed top-0 left-0 w-full z-50 glass-panel border-b-0">
    <div class="max-w-7xl mx-auto px-6 md:px-12 py-4 flex justify-between items-center">
      <router-link to="/" class="text-xl font-bold text-primary tracking-tighter hover:text-accent transition-colors">
        SG<span class="text-accent">.</span>
      </router-link>
      
      <div class="hidden md:flex gap-8 text-sm font-medium text-secondary">
        <router-link v-for="link in links" :key="link.name" :to="link.path" class="hover:text-primary transition-colors" active-class="text-accent">
          {{ link.name }}
        </router-link>
      </div>

      <button class="md:hidden text-primary">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>
      </button>
    </div>
  </nav>
</template>

<script setup>
const links = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Projects', path: '/projects' },
  { name: 'Skills', path: '/skills' },
//   { name: 'Blog', path: '/blog' },
//   { name: 'Resume', path: '/resume' },
  { name: 'Contact', path: '/contact' },
]
</script>