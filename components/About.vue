<template>
  <section id="about" class="py-8 bg-slate-900">
    <div class="max-w-5xl mx-auto px-6">
      <div class="grid md:grid-cols-3 gap-6 items-start">
        <div class="md:col-span-2">
          <h2 class="text-2xl font-bold text-slate-100">About</h2>
          <div class="mt-3 text-slate-300 text-base md:text-lg space-y-3 leading-relaxed">
            <p>I'm a backend engineer and DevOps practitioner who builds scalable services and automations. I design APIs, implement CI/CD pipelines, and manage infrastructure as code with a focus on reliability and observability.</p>
            <p>Rather than flashy front-end demos, my work shows up as dependable systems: tests that catch regressions, deployments that don't fail at 2AM, and infrastructure that is versioned and reviewable.</p>
          </div>
        </div>

        <!-- Increased font size only, reduced padding and margins for the capabilities box -->
        <aside class="rounded-lg border border-slate-700 bg-slate-800 p-4">
          <div class="text-slate-300 text-lg font-semibold">Capabilities</div>
          <ul class="mt-3 space-y-2 text-slate-200 text-base leading-relaxed">
            <li>• API implementation (REST)</li>
            <li>• Infrastructure as Code (Terraform)</li>
            <li>• CI/CD & GitOps (GitHub Actions, Jenkins)</li>
            <li>• Containerization & Orchestration (Docker, K8s)</li>
            <li>• Learning cloud technologies like AWS, Oracle and GCP</li>
          </ul>
        </aside>
      </div>
    </div>
  </section>
</template>
