<template>
  <section id="contact" class="py-8 bg-slate-800">
    <div class="max-w-5xl mx-auto px-6">
      <h2 class="text-2xl font-bold text-slate-100">Contact</h2>
      <p class="mt-1 text-slate-300">Connect with me!</p>

      <div class="mt-4 relative">
        <pre class="rounded-lg bg-slate-900 p-6 text-sm text-slate-200 overflow-auto"><code v-html="highlightedHtml"></code></pre>

        <div class="absolute top-3 right-3 flex items-center gap-2">
          <button @click="copyJson" class="bg-indigo-600 text-white px-3 py-1 rounded text-sm hover:bg-indigo-500">Copy</button>
          <span v-if="copied" class="text-xs text-slate-400">Copied!</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'

const data = {
  status: "200 OK",
  contact: {
    email: "vprerana23@gmail.com",
    linkedin: "www.linkedin.com/in/prerana-vyavahare-15a087243/",
    github: "https://github.com/PreVya"
  },
  preferred: ["email", "LinkedIn","github"],
  timezone: "IST - Indian Standard Time (GMT+5:30)",
  currently_located_in:"Thane, Maharashtra,India",
  open_to_relocate:true
}

const copied = ref(false)

function escapeHtml(str) {
  return String(str).replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;')
}

const highlightedHtml = computed(() => {
  const json = JSON.stringify(data, null, 2)
  // escape first
  let html = escapeHtml(json)

  // Highlight the contact block specially and make values clickable
  html = html.replace(/("contact": \{[\s\S]*?\})/, (match) => {
    let inner = match.replace(/"(email|linkedin|github)": \"(.*?)\"/g, (m, key) => {
      // use actual data values for href and display (avoid relying on the escaped match)
      const raw = data.contact[key]
      const display = escapeHtml(raw)
      let href = raw
      if (key === 'email') href = `mailto:${raw}`
      else if (!/^https?:\/\//.test(raw)) href = `https://${raw}`
      return `<span class="text-slate-300">\"${key}\"</span>: <a href=\"${href}\" class=\"text-indigo-100 underline\" target=\"_blank\" rel=\"noopener\">\"${display}\"</a>`
    })
    // wrap the whole contact object with a subtle block highlight
    return `<span class=\"inline-block bg-indigo-800/30 px-2 py-1 rounded\">${inner}</span>`
  })

  // highlight other keys and string values
  html = html
    .replace(/\"(\w+)\"(?=:\s)/g, '<span class="text-slate-400">"$1"</span>')
    .replace(/: \"(.*?)\"/g, ': <span class="text-slate-300">"$1"</span>')

  // highlight numbers/booleans
  html = html.replace(/: (\d+|true|false|null)/g, ': <span class="text-slate-400">$1</span>')

  return html
})

async function copyJson() {
  try {
    await navigator.clipboard.writeText(JSON.stringify(data, null, 2))
    copied.value = true
    setTimeout(() => (copied.value = false), 1500)
  } catch (e) {
    // ignore
  }
}
</script>
