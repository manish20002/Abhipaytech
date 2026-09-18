<script setup lang="ts">
import { ref } from 'vue'

const navItems = [
  { label: 'Home', href: '#home' },
  { label: 'About', href: '#about' },
  { label: 'Financial', href: '#financial' },
  { label: 'Company Profile', href: '#company-profile' },
  { label: 'Solutions', href: '#solutions' },
  { label: 'Contact', href: '#contact' },
]

const isMenuOpen = ref(false)
</script>

<template>
  <nav class="fixed top-0 z-50 w-full border-b border-slate-800 bg-slate-950/80 backdrop-blur-xl">
    <div class="mx-auto flex max-w-7xl items-center justify-between px-4 py-3 sm:px-6 lg:px-8">
      <a href="#home" class="flex items-center gap-3" @click="isMenuOpen = false">
        <img src="./images/Abhipaytech_logo.png" alt="AbhiPay logo" class="h-9 w-9 rounded-lg bg-white p-1 object-contain" />
        <span class="text-base font-semibold text-white sm:text-lg">AbhiPayTech</span>
      </a>

      <div class="hidden items-center gap-5 lg:flex">
        <a v-for="item in navItems" :key="item.href" :href="item.href" class="text-sm font-medium text-slate-200 transition hover:text-white">{{ item.label }}</a>
      </div>

      <div class="flex items-center gap-2 sm:gap-3">
        <a href="#contact" class="hidden rounded-full bg-indigo-500 px-3 py-2 text-xs font-semibold text-white transition hover:bg-indigo-400 sm:inline-flex sm:text-sm">
          Get Started
        </a>

        <button
          type="button"
          class="inline-flex h-10 w-10 items-center justify-center rounded-full border border-slate-700 bg-slate-900 text-slate-100 lg:hidden"
          aria-label="Toggle menu"
          :aria-expanded="isMenuOpen"
          @click="isMenuOpen = !isMenuOpen"
        >
          <svg v-if="!isMenuOpen" class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
            <path d="M4 7h16M4 12h16M4 17h16" />
          </svg>
          <svg v-else class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
    </div>

    <div v-if="isMenuOpen" class="border-t border-slate-800 bg-slate-950 lg:hidden">
      <div class="mx-auto flex max-w-7xl flex-col gap-2 px-4 py-4 sm:px-6">
        <a
          v-for="item in navItems"
          :key="item.href"
          :href="item.href"
          class="rounded-xl px-3 py-2 text-sm font-medium text-slate-200 transition hover:bg-slate-900 hover:text-white"
          @click="isMenuOpen = false"
        >
          {{ item.label }}
        </a>
      </div>
    </div>
  </nav>
</template>
