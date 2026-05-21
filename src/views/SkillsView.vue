<template>
  <div class="py-12 animate-fade-in-up">
    <h2 class="text-3xl md:text-4xl font-bold mb-2">Technical Arsenal</h2>
    <p class="text-secondary mb-12">Technologies and tools I work with on a daily basis.</p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div v-for="(category, idx) in skillCategories" :key="idx" class="glass-panel p-6 rounded-2xl">
        <h3 class="text-xl font-bold text-primary mb-6 flex items-center gap-2">
          <span class="w-8 h-px bg-accent"></span> {{ category.title }}
        </h3>
        <div class="flex flex-wrap gap-3">
          <span v-for="skill in category.skills" :key="skill" class="px-4 py-2 rounded-lg bg-surface/50 border border-white/5 text-secondary text-sm hover:text-accent hover:border-accent/30 transition-all cursor-default">
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const skillCategories = [
  { title: 'Frontend', skills: ['VueJS', 'TailwindCSS', 'JavaScript', 'HTML5/CSS3'] },
  { title: 'Backend', skills: ['Python', 'Flask', 'Redis', 'Celery'] },
  { title: 'Data & ML', skills: ['Machine Learning', 'Scikit-Learn', 'SQL', 'Data Analytics'] },
  { title: 'AI & LLMs', skills: ['LangChain', 'LangGraph', 'Prompt Engineering'] },
  { title: 'Tools & Others', skills: ['Git/GitHub', 'Advanced Excel', 'System Commands'] }
]
</script>