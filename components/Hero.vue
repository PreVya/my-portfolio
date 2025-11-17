<template>
  <section id="home" class="min-h-[40vh] flex items-center pt-6">
    <div class="max-w-5xl mx-auto px-6">
      <div class="grid gap-6 md:grid-cols-2 items-center">
        <div>
          <h1 class="text-4xl md:text-5xl font-bold text-slate-100 leading-tight">Hi, I'm Prerana — Backend developer & DevOps and cloud enthusiast</h1>
          <p class="mt-4 text-lg text-slate-300">I build resilient APIs, design scalable infrastructure and automate reliable deployments. I focus on observability, performance and pragmatic tooling.</p>

          <div class="mt-4 flex gap-3">
            <a href="#projects" class="inline-block bg-indigo-600 text-white px-4 py-2 rounded-lg shadow hover:shadow-lg transition">See my projects</a>
            <a href="#contact" class="inline-block text-indigo-300 px-4 py-2 rounded-lg border border-indigo-800 hover:bg-indigo-900 transition">Get in touch</a>
          </div>

          <!-- <div class="mt-4 flex flex-wrap gap-2">
            <span class="text-xs px-2 py-1 bg-slate-700 rounded text-slate-200">APIs</span>
            <span class="text-xs px-2 py-1 bg-slate-700 rounded text-slate-200">IaC</span>
            <span class="text-xs px-2 py-1 bg-slate-700 rounded text-slate-200">CI/CD</span>
          </div> -->
        </div>

        <div class="flex flex-col items-center md:items-end">
          <!-- Arch user small label (moved above terminal) -->
          <div class="w-full max-w-xs mb-2 flex justify-center">
            <div class="flex items-center gap-2">
              <svg class="w-5 h-5 text-cyan-400" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden>
                <path d="M128 24L32 200h48l16-32h64l16 32h48L128 24z" fill="currentColor" />
                <path d="M128 72l24 52H104l24-52z" fill="#0EA5A4" opacity="0.9" />
              </svg>
              <span class="text-sm text-slate-400">I am an Arch user!</span>
            </div>
          </div>

          <div class="w-full max-w-xs bg-slate-900 border border-slate-700 rounded-lg p-4 font-mono text-sm text-slate-200 shadow-lg">
            <div class="flex items-center justify-between mb-3">
              <div class="flex items-center gap-2">
                <span class="w-2 h-2 bg-red-500 rounded-full"></span>
                <span class="w-2 h-2 bg-yellow-400 rounded-full"></span>
                <span class="w-2 h-2 bg-green-400 rounded-full"></span>
              </div>
              <span class="text-xs text-slate-400">arch@machine</span>
            </div>

            <pre class="whitespace-pre-wrap"><code class="block">$ sudo pacman -Syu
$ sudo pacman -S docker minikube kubectl kubens 
$ sudo systemctl enable docker
$ sudo minikube start --nodes=2 --driver=docker
</code></pre>

            <!-- <div class="mt-3 flex justify-end">
              <button class="text-xs bg-indigo-600 px-2 py-1 rounded hover:bg-indigo-500">Copy snippet</button>
            </div> -->
          </div>

          <div class="mt-4 flex gap-2 text-xs">
            <span class="px-2 py-1 bg-indigo-700 text-indigo-100 rounded">Docker</span>
            <span class="px-2 py-1 bg-emerald-700 text-emerald-100 rounded">Kubernetes</span>
            <span class="px-2 py-1 bg-violet-700 text-violet-100 rounded">Terraform</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
