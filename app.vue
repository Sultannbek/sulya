<script setup lang="ts">
const experience = [
  { role: 'Founding Designer', company: 'Athena Labs', logo: '/logos/athena-labs.svg', note: 'Physical AI startup' },
  { role: 'SMM & Design Lead', company: 'Investly Hub', logo: '/logos/investly-hub.jpg' },
  { role: 'Designer', company: '1609+', logo: '/logos/1609.svg', logoOnly: true },
]

const links = [
  { label: 'github', href: 'https://github.com/Sultannbek' },
  { label: 'twitter', href: 'https://x.com/sulyaa__' },
  { label: 'linkedin', href: 'https://www.linkedin.com/in/sultanbek-bazarbaev-5852473a6' },
  { label: 'instagram', href: 'https://www.instagram.com/sulyyaa_/' },
]
</script>

<template>
  <main class="flex min-h-screen items-center px-6 py-16 sm:px-16 lg:px-24">
    <div class="text-[17px] leading-7">
      <h1 class="font-medium text-neutral-900">sulya</h1>
      <p class="mt-3 text-neutral-500">student, tech enthusiast, designer</p>

      <ul class="mt-10 space-y-1">
        <li v-for="job in experience" :key="job.company" class="text-neutral-500">
          <span class="text-neutral-900">{{ job.role }}</span> <img
            :src="job.logo"
            :alt="job.logoOnly ? job.company : ''"
            :class="job.logoOnly ? 'h-5 w-auto align-[1px]' : 'mr-1 h-[18px] w-[18px] align-[-4px]'"
            class="inline-block mix-blend-multiply"
          ><template v-if="!job.logoOnly">{{ job.company }}</template><span v-if="job.note" class="text-neutral-400"> — {{ job.note }}</span>
        </li>
      </ul>

      <ul class="mt-10 space-y-2.5">
        <li v-for="link in links" :key="link.label">
          <a
            :href="link.href"
            target="_blank"
            rel="noopener noreferrer"
            class="text-neutral-900 underline decoration-neutral-300 underline-offset-4 transition-colors hover:decoration-neutral-900"
          >{{ link.label }}</a>
        </li>
      </ul>

      <div class="mt-10">
        <SpotifyPlayer />
      </div>
    </div>
  </main>
</template>

<style>
html {
  background-color: #f5f5f4;
  font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Text', 'SF Pro Display', system-ui, sans-serif;
  -webkit-font-smoothing: antialiased;
}
</style>
