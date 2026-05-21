<template>
  <div class="flex flex-col items-start justify-center min-h-[80vh] animate-fade-in-up">
    <p class="text-accent font-mono mb-4 text-lg">Hi, my name is</p>
    <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight mb-4">
      Shivam Gupta.
    </h1>
    <h2 class="text-4xl md:text-6xl font-bold text-secondary mb-6">
      Building scalable systems & AI solutions.
    </h2>
    <p class="text-secondary max-w-2xl text-lg md:text-xl leading-relaxed mb-10">
      I'm a Data Science student at IIT Madras and a full-stack developer. I love building web applications that combine clean code with smart machine learning to solve real-world problems.
    </p>
    
    <div class="flex gap-4">
      <router-link to="/projects" class="px-8 py-3 rounded-lg bg-accent text-white font-semibold hover:bg-blue-600 transition-colors shadow-lg shadow-accent/20">
        Check out my work
      </router-link>
      <a href="/resume.pdf" target="_blank" class="px-8 py-3 rounded-lg glass-panel hover:bg-white/5 transition-colors font-semibold">
        Download Resume
      </a>
    </div>

    <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-4 w-full max-w-3xl border-t border-white/10 pt-8">
      <div v-for="skill in coreSkills" :key="skill" class="text-secondary font-mono text-sm flex items-center gap-2">
        <span class="w-2 h-2 rounded-full bg-accent"></span> {{ skill }}
      </div>
    </div>
  </div>
</template>

<script setup>
const coreSkills = ['Python & Flask', 'Vue 3 & Tailwind', 'Machine Learning', 'Data Architecture']
</script>