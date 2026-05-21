<template>
  <div class="py-12 animate-fade-in-up">
    <h2 class="text-3xl md:text-4xl font-bold mb-2">Featured Projects</h2>
    <p class="text-secondary mb-12">Some things I've built integrating data, web technologies, and automation pipelines.</p>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div 
        v-for="project in projects" 
        :key="project.title"
        class="glass-panel p-6 rounded-2xl group hover:border-accent/50 transition-all duration-300 transform hover:-translate-y-2 flex flex-col h-full relative"
      >
        <p class="text-accent font-mono text-sm mb-2 opacity-80">{{ project.date }}</p>

        <h3 class="text-2xl font-bold text-primary mb-3 group-hover:text-accent transition-colors">
          {{ project.title }}
        </h3>
        <p class="text-secondary mb-6 flex-grow">
          {{ project.description }}
        </p>
        
        <div class="flex flex-wrap gap-2 mb-6">
          <span 
            v-for="tech in project.tech" 
            :key="tech"
            class="px-3 py-1 rounded-full bg-accent/10 text-accent text-xs font-mono font-medium"
          >
            {{ tech }}
          </span>
        </div>
        
        <div class="flex gap-4 mt-auto">
          <a 
            :href="project.github" 
            target="_blank" 
            rel="noopener noreferrer" 
            class="text-primary hover:text-accent transition-colors flex items-center gap-2 text-sm font-semibold"
          >
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
            </svg>
            Code
          </a>
          <a 
            v-if="project.live" 
            :href="project.live" 
            target="_blank" 
            rel="noopener noreferrer" 
            class="text-primary hover:text-accent transition-colors flex items-center gap-2 text-sm font-semibold"
          >
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
            </svg>
            Live Demo
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const projects = [
  {
    title: 'Instagram Reels View Scraping Pipeline',
    date: 'May 2026',
    description: 'An automated web collection engine optimized for crawling real-time user metrics, view frequencies, and social visibility data from video feeds. Designed to package clean analytics layers while bypassing delivery anti-bot rate boundaries.',
    tech: ['Python', 'Web Scraping', 'Automation', 'Data Processing'],
    github: 'https://github.com/shivam91264/insta_reels_view_scraping',
    live: null
  },
  {
    title: 'Full-Stack eCommerce Platform',
    date: 'Feb 2026',
    description: 'A complete clothing eCommerce platform featuring an intuitive admin panel dashboard, robust secure authentication, dynamic order workflows, precise stock inventory handling, and a highly responsive layout context built atop a modular architecture.',
    tech: ['Flask', 'VueJS', 'SQLite', 'Bootstrap'],
    github: 'https://github.com/shivam91264/E-Commerce',
    live: null
  },
  {
    title: 'Vehicle Parking App – V2',
    date: 'Nov 2025',
    description: 'An intelligent parking management system optimizing slot layouts. Features an active booking terminal, administrative configuration monitors, background email notifications, detailed structural report generation, and asynchronous queue execution.',
    tech: ['Flask', 'VueJS', 'Redis', 'Celery'],
    github: 'https://github.com/shivam91264/MAD-2-VEHICLE-PARKING-APP',
    live: null
  },
  {
    title: 'Influencer Engagement Platform',
    date: 'Sep 2025',
    description: 'A structural brand partnership and sponsor synchronization portal. Connects content creators with strategic advertisers, incorporating full campaign cycle management, operational checks, and administrative control settings.',
    tech: ['Flask', 'Jinja2', 'SQLAlchemy'],
    github: 'https://github.com/shivam91264/Influencer-Engagement-Sponsor-Coordination-Flask-Project',
    live: null
  },
  {
    title: 'Battery Shop Data Analytics',
    date: 'Jul 2025',
    description: 'A comprehensive business intelligence and supply chain optimization context built around field enterprise metrics. Applies machine learning workflows and exploratory models to forecast demand matrices and smooth storage cycles.',
    tech: ['Python', 'Excel', 'Machine Learning', 'Data Analysis'],
    github: 'https://github.com/shivam91264/BDM-PROJECT',
    live: null
  }
]
</script>