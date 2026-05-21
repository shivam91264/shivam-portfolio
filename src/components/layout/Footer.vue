<template>
  <footer class="mt-auto border-t border-white/10 bg-surface/30 backdrop-blur-md">
    <div class="max-w-7xl mx-auto px-6 md:px-12 py-8 flex flex-col md:flex-row justify-between items-center gap-4">
      
      <div class="text-secondary text-sm font-medium">
        &copy; {{ currentYear }} Shivam Gupta. All rights reserved.
      </div>
      
      <div class="flex gap-6 text-sm font-medium text-secondary">
        <a 
          href="https://github.com/shivam91264" 
          target="_blank" 
          rel="noopener noreferrer" 
          class="hover:text-primary hover:text-accent transition-colors"
        >
          GitHub
        </a>
        <a 
          href="https://linkedin.com/in/shivam-gupta-10b87a391" 
          target="_blank" 
          rel="noopener noreferrer" 
          class="hover:text-primary hover:text-accent transition-colors"
        >
          LinkedIn
        </a>
        <a 
          href="mailto:sg426445@gmail.com" 
          class="hover:text-primary hover:text-accent transition-colors"
        >
          Email
        </a>
      </div>

    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

// Dynamically get the current year so you never have to update it manually
const currentYear = computed(() => new Date().getFullYear())
</script>