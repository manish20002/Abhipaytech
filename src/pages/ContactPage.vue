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
      <div class="grid gap-10 lg:grid-cols-[1.1fr_0.9fr]">
        <div class="rounded-3xl bg-slate-900 p-8 text-white shadow-xl shadow-slate-200 sm:p-10">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-300">Contact</p>
          <h1 class="mt-4 text-4xl font-black tracking-tight sm:text-5xl">
            Let’s build your next growth milestone.
          </h1>
          <p class="mt-5 max-w-xl text-lg leading-8 text-slate-300">
            Tell us what you need, and our team will help you create a smarter, faster, and more
            scalable payment or operations strategy.
          </p>

          <div class="mt-10 space-y-5 text-slate-200">
            <div class="flex items-center gap-3">
              <span class="h-2.5 w-2.5 rounded-full bg-indigo-400"></span>
              <span><span class="font-semibold text-white">Email:</span> hello@abhipaytech.com</span>
            </div>
            <div class="flex items-center gap-3">
              <span class="h-2.5 w-2.5 rounded-full bg-indigo-400"></span>
              <span><span class="font-semibold text-white">Phone:</span> +91 98765 43210</span>
            </div>
            <div class="flex items-center gap-3">
              <span class="h-2.5 w-2.5 rounded-full bg-indigo-400"></span>
              <span><span class="font-semibold text-white">Address:</span> Pune, Maharashtra, India</span>
            </div>
          </div>
        </div>

        <form class="rounded-3xl bg-white p-8 shadow-lg shadow-slate-200 ring-1 ring-slate-200 sm:p-10">
          <div class="space-y-5">
            <div>
              <label class="mb-2 block text-sm font-medium text-slate-700">Full Name</label>
              <input
                type="text"
                placeholder="Your name"
                class="w-full rounded-xl border border-slate-200 bg-slate-50 px-4 py-3 text-slate-900 outline-none transition focus:border-indigo-400 focus:ring-2 focus:ring-indigo-100"
              />
            </div>

            <div>
              <label class="mb-2 block text-sm font-medium text-slate-700">Email</label>
              <input
                type="email"
                placeholder="you@example.com"
                class="w-full rounded-xl border border-slate-200 bg-slate-50 px-4 py-3 text-slate-900 outline-none transition focus:border-indigo-400 focus:ring-2 focus:ring-indigo-100"
              />
            </div>

            <div>
              <label class="mb-2 block text-sm font-medium text-slate-700">Message</label>
              <textarea
                rows="5"
                placeholder="Tell us about your project"
                class="w-full rounded-xl border border-slate-200 bg-slate-50 px-4 py-3 text-slate-900 outline-none transition focus:border-indigo-400 focus:ring-2 focus:ring-indigo-100"
              ></textarea>
            </div>

            <button
              type="button"
              class="w-full rounded-full bg-indigo-600 px-6 py-3 text-sm font-semibold text-white shadow-lg shadow-indigo-200 transition hover:bg-indigo-500"
            >
              Send Message
            </button>
          </div>
        </form>
      </div>
    </section>
  </main>
</template>
