<template>
  <div class="py-12 animate-fade-in-up">
    <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-12 gap-4">
      <div>
        <h2 class="text-3xl md:text-4xl font-bold mb-2">Writings</h2>
        <p class="text-secondary">Thoughts on software engineering, AI, and my journey.</p>
      </div>
      
      <div class="relative w-full md:w-64">
        <input type="text" placeholder="Search articles..." class="w-full bg-surface/50 border border-white/10 rounded-lg py-2 px-4 text-sm text-primary focus:outline-none focus:border-accent transition-colors">
      </div>
    </div>

    <div class="space-y-6">
      <article v-for="post in posts" :key="post.title" class="glass-panel p-6 rounded-2xl group cursor-pointer hover:border-accent/30 transition-all">
        <p class="text-sm text-accent font-mono mb-2">{{ post.date }} • {{ post.readTime }}</p>
        <h3 class="text-2xl font-bold text-primary mb-3 group-hover:text-accent transition-colors">{{ post.title }}</h3>
        <p class="text-secondary mb-4">{{ post.excerpt }}</p>
        <div class="flex gap-2">
          <span v-for="tag in post.tags" :key="tag" class="text-xs text-secondary bg-surface px-2 py-1 rounded">{{ tag }}</span>
        </div>
      </article>
    </div>
  </div>
</template>

<script setup>
const posts = [
  {
    title: 'Building Full Stack Apps with Flask and Vue',
    excerpt: 'A comprehensive guide to connecting a Python backend with a reactive JavaScript frontend.',
    date: 'Oct 12, 2025',
    readTime: '5 min read',
    tags: ['Web Dev', 'Flask', 'Vue']
  },
  {
    title: 'My IIT Madras Journey: Navigating Data Science',
    excerpt: 'Reflections and lessons learned during my BS degree program so far.',
    date: 'Sep 28, 2025',
    readTime: '8 min read',
    tags: ['Personal', 'IIT Madras']
  },
  {
    title: 'Beginner Guide to Machine Learning Pipelines',
    excerpt: 'How to structure your ML code using Scikit-Learn for scalable deployments.',
    date: 'Aug 15, 2025',
    readTime: '6 min read',
    tags: ['Machine Learning', 'Python']
  }
]
</script>