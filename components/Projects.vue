<template>
  <section id="projects" class="py-8 bg-slate-800">
    <div class="max-w-5xl mx-auto px-6">
      <h2 class="text-2xl font-bold text-slate-100">Projects</h2>
      <p class="mt-1 text-slate-300">A selection of projects — click any card to open the git repository of my projects.</p>

      <div class="mt-4 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
        <a v-for="(p, i) in projects" :key="i" :href="p.link" target="_blank" rel="noopener" class="group block p-4 rounded-2xl border border-slate-700 bg-slate-900 shadow-sm hover:shadow-lg transition transform hover:-translate-y-1">
          <div class="flex items-center justify-between">
            <h3 class="text-lg font-semibold text-slate-100">{{ p.title }}</h3>
            <span class="text-sm text-slate-400">{{ p.year }}</span>
          </div>

          <p class="mt-2 text-slate-300">{{ p.description }}</p>

          <div class="mt-3 flex flex-wrap gap-2">
            <span v-for="(t, j) in p.tech" :key="j" class="text-xs px-2 py-1 bg-slate-700 text-slate-200 rounded">{{ t }}</span>
          </div>

          <div class="mt-4 flex items-center justify-between">
            <span class="text-sm text-indigo-400 group-hover:underline">View repo</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-slate-400 group-hover:text-indigo-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 3h7v7m0 0L10 21l-7-7 11-11z" />
            </svg>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  { title: 'MGNREGA-backend', description: 'Fetches data about a district from data.gov.in official site and saves to NeonDB database. Acts as backend to MGNREGA-frontennd and provides it with data for visualization.', tech: ['Python','FastAPI','NeonDB','Redis'], year: '2025', link: 'https://github.com/PreVya/MGNREGA-backend' },
  { title: 'MGNREGA-frontend', description: 'District wise data visualization. Fetches this data from the MGNREGA-backend.', tech: ['Python', 'Streamlit'], year: '2025', link: 'https://github.com/PreVya/MGNREGA-frontend' },
  { title: 'terraform-files', description: 'Different brances of this repo contains 3 different infrastructure for deployment of 2 simple apps. Deployment infrastucture involve deploying on same EC2 instance of AWS, two different EC2 instance and lastly deploying apps with 2 task definitions in a ECS cluster.', tech: ['Terraform'], year: '2025', link: 'https://github.com/PreVya/terraform-files/tree/main' },
  { title: 'MicroORM-book-author', description: 'Simple book-author backend app made using NestJS. Application of CRUD, authentication, RoleAuth and redis caching.', tech: ['TypeScript','NestJS'], year: '2024', link: 'https://github.com/PreVya/mikroORM-book-author' },
  { title: 'Project Five', description: 'Short description about project five.', tech: ['Python', 'Flask'], year: '2024', link: '#' },
  { title: 'Project Six', description: 'Short description about project six.', tech: ['Go', 'Docker'], year: '2023', link: '#' }
]
</script>
