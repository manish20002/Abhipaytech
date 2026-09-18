<script setup lang="ts">
import { ref } from 'vue'
import Navbar from '../Navbar.vue'

const props = defineProps<{
  activePage?: 'home' | 'about' | 'contact'
}>()

const faqs = [
  { question: 'How quickly can I get started?', answer: 'Most clients are set up within a few business days, depending on the scope of the integration.' },
  { question: 'Do you support growing businesses?', answer: 'Yes. Our system is designed for startups, SMEs, and scaling teams with flexible workflows.' },
  { question: 'Is the platform secure?', answer: 'Absolutely. We prioritize secure payment processing, data protection, and operational reliability.' },
]

const openFaq = ref(0)

const emit = defineEmits<{
  (event: 'home'): void
  (event: 'about'): void
  (event: 'contact'): void
}>()
</script>

<template>
  <main>
    <Navbar :active-page="props.activePage ?? 'home'" @home="$emit('home')" @about="$emit('about')" @contact="$emit('contact')" />

    <section id="home" class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
      <div class="grid items-center gap-10 lg:grid-cols-2">
        <div>
          <p class="mb-4 inline-flex rounded-full bg-indigo-100 px-3 py-1 text-sm font-semibold text-indigo-700">
            Smart financial solutions
          </p>
          <h1 class="text-4xl font-black tracking-tight text-slate-900 sm:text-5xl">
            Growth that moves as fast as your business.
          </h1>
          <p class="mt-6 max-w-xl text-lg text-slate-600">
            AbhiPay helps businesses simplify payments, automate finance workflows, and scale with confidence.
          </p>
          <div class="mt-8 flex flex-wrap gap-4">
            <button class="rounded-full bg-indigo-600 px-6 py-3 text-sm font-semibold text-white shadow-lg shadow-indigo-200 transition hover:bg-indigo-500">
              Get Started
            </button>
            <button class="rounded-full border border-slate-300 bg-white px-6 py-3 text-sm font-semibold text-slate-700 transition hover:border-indigo-200 hover:text-indigo-600">
              Book a Demo
            </button>
          </div>
        </div>

        <div class="rounded-3xl bg-white p-6 shadow-xl shadow-slate-200 ring-1 ring-slate-200">
          <img src="/images/Abhipaytech_logo.png" alt="Abhi Pay Tech Private Limited" class="w-full rounded-2xl" />
        </div>
      </div>
    </section>

    <section class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8">
      <div class="mb-10 text-center">
        <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-600">Solutions</p>
        <h2 class="mt-3 text-3xl font-bold text-slate-900">Built for speed, clarity, and growth</h2>
      </div>

      <div class="grid gap-6 md:grid-cols-3">
        <article class="rounded-2xl bg-white p-6 shadow-sm ring-1 ring-slate-200">
          <div class="mb-4 h-12 w-12 rounded-xl bg-indigo-100 text-2xl">⚡</div>
          <h3 class="text-xl font-semibold text-slate-900">Fast Payments</h3>
          <p class="mt-3 text-slate-600">Reduce friction with secure, instant payment processing built for modern businesses.</p>
        </article>

        <article class="rounded-2xl bg-white p-6 shadow-sm ring-1 ring-slate-200">
          <div class="mb-4 h-12 w-12 rounded-xl bg-emerald-100 text-2xl">📊</div>
          <h3 class="text-xl font-semibold text-slate-900">Insights</h3>
          <p class="mt-3 text-slate-600">Track performance, cash flow, and operational trends with real-time reporting dashboards.</p>
        </article>

        <article class="rounded-2xl bg-white p-6 shadow-sm ring-1 ring-slate-200">
          <div class="mb-4 h-12 w-12 rounded-xl bg-amber-100 text-2xl">🔒</div>
          <h3 class="text-xl font-semibold text-slate-900">Secure Operations</h3>
          <p class="mt-3 text-slate-600">Protect transactions with compliance-first infrastructure and trusted workflows.</p>
        </article>
      </div>
    </section>

    <section class="mx-auto max-w-5xl px-4 py-16 sm:px-6 lg:px-8">
      <div class="mb-8 text-center">
        <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-600">FAQ</p>
        <h2 class="mt-3 text-3xl font-bold text-slate-900">Frequently asked questions</h2>
      </div>

      <div class="space-y-4">
        <div v-for="(faq, index) in faqs" :key="faq.question" class="overflow-hidden rounded-2xl border border-slate-200 bg-white shadow-sm">
          <button
            type="button"
            class="flex w-full items-center justify-between px-5 py-4 text-left text-slate-900"
            @click="openFaq = openFaq === index ? -1 : index"
          >
            <span class="font-semibold">{{ faq.question }}</span>
            <span class="text-xl text-indigo-600">{{ openFaq === index ? '−' : '+' }}</span>
          </button>
          <div v-if="openFaq === index" class="border-t border-slate-200 px-5 py-4 text-slate-600">
            {{ faq.answer }}
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
