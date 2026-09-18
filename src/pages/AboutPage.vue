<script setup lang="ts">
import Navbar from '../Navbar.vue'

const props = defineProps<{
  activePage?: 'home' | 'about' | 'contact'
}>()
</script>

<template>
  <main class="bg-slate-50">
    <Navbar :active-page="props.activePage ?? 'home'" @home="$emit('home')" @about="$emit('about')" @contact="$emit('contact')" />

    <section class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
      <div class="mb-12 max-w-3xl">
        <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-600">About us</p>
        <h1 class="mt-4 text-4xl font-black tracking-tight text-slate-900 sm:text-5xl">
          We simplify financial operations for growing businesses.
        </h1>
        <p class="mt-6 text-lg leading-8 text-slate-600">
          AbhiPay helps startups and established companies move faster with secure payment tools,
          intelligent reporting, and support designed around real business needs.
        </p>
      </div>

      <div class="grid gap-10 lg:grid-cols-2">
        <div class="rounded-3xl bg-white p-8 shadow-lg shadow-slate-200 ring-1 ring-slate-200">
          <h2 class="text-2xl font-bold text-slate-900">Our mission</h2>
          <p class="mt-5 text-slate-600">
            To make financial transactions more transparent, efficient, and accessible for every
            modern business.
          </p>
          <div class="mt-8 space-y-5">
            <div class="flex gap-4">
              <div class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-indigo-100 text-indigo-600">✓</div>
              <div>
                <h3 class="font-semibold text-slate-900">Built for speed</h3>
                <p class="mt-1 text-slate-600">Streamlined workflows reduce friction and improve turnaround time.</p>
              </div>
            </div>
            <div class="flex gap-4">
              <div class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-emerald-100 text-emerald-600">✓</div>
              <div>
                <h3 class="font-semibold text-slate-900">Built for trust</h3>
                <p class="mt-1 text-slate-600">Secure infrastructure and compliance-first habits keep operations protected.</p>
              </div>
            </div>
          </div>
        </div>

        <div class="rounded-3xl bg-slate-900 p-8 text-white shadow-xl shadow-slate-200">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-300">Why choose us</p>
          <div class="mt-8 space-y-6">
            <div>
              <p class="text-3xl font-black text-white">10+</p>
              <p class="mt-2 text-slate-300">Years of digital finance experience</p>
            </div>
            <div>
              <p class="text-3xl font-black text-white">24/7</p>
              <p class="mt-2 text-slate-300">Responsive customer support</p>
            </div>
            <div>
              <p class="text-3xl font-black text-white">99.9%</p>
              <p class="mt-2 text-slate-300">Operational reliability</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
