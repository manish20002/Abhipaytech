<script setup lang="ts">
import Navbar from './Navbar.vue'

const solutions = [
  {
    title: 'Fast Payments',
    description: 'Enable faster checkout, automated settlement, and better customer trust with secure payment processing.',
    icon: '⚡',
    tone: 'from-indigo-500/20 to-blue-500/5',
  },
  {
    title: 'Business Insights',
    description: 'Track revenue, cash flow, and transaction trends in one simple view built for modern teams.',
    icon: '📊',
    tone: 'from-emerald-500/20 to-green-500/5',
  },
  {
    title: 'Reliable Support',
    description: 'Get strategic guidance and dependable operational support as your business scales up.',
    icon: '🔒',
    tone: 'from-amber-500/20 to-yellow-500/5',
  },
]

const faqs = [
  {
    question: 'How quickly can we begin?',
    answer: 'Most clients are onboarded in a few business days depending on the integration and support requirements.',
  },
  {
    question: 'Do you support growing businesses?',
    answer: 'Yes. Our workflows are designed for startups, SMBs, and scaling enterprises that need flexibility.',
  },
  {
    question: 'Is the platform secure?',
    answer: 'Absolutely. Security, compliance, and dependable infrastructure are at the center of our solution design.',
  },
]
</script>

<template>
  <div class="min-h-screen bg-slate-950 text-slate-100">
    <Navbar />

    <main class="pt-24">
      <section id="home" class="relative overflow-hidden">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_top,_rgba(99,102,241,0.28),transparent_40%)]"></div>
        <div class="relative mx-auto grid max-w-7xl gap-12 px-4 py-20 sm:px-6 lg:grid-cols-2 lg:px-8 lg:py-28">
          <div class="flex flex-col justify-center">
            <span class="mb-5 inline-flex w-fit rounded-full border border-indigo-400/30 bg-indigo-500/10 px-4 py-2 text-sm font-medium text-indigo-200">
              Smart financial solutions
            </span>
            <h1 class="text-4xl font-black tracking-tight text-white sm:text-5xl lg:text-6xl">
              Growth that moves at the speed of business.
            </h1>
            <p class="mt-6 max-w-xl text-lg leading-8 text-slate-300">
              AbhiPay helps businesses simplify payments, streamline financial operations, and build confident momentum for the next stage of growth.
            </p>
            <div class="mt-8 flex flex-wrap gap-4">
              <a href="#contact" class="rounded-full bg-indigo-500 px-6 py-3 text-sm font-semibold text-white shadow-lg shadow-indigo-500/30 transition hover:bg-indigo-400">
                Get Started
              </a>
              <a href="#about" class="rounded-full border border-slate-700 bg-slate-900/70 px-6 py-3 text-sm font-semibold text-slate-100 transition hover:border-indigo-400 hover:text-white">
                Learn More
              </a>
            </div>
          </div>

          <div class="rounded-3xl border border-slate-800 bg-white/5 p-6 shadow-2xl shadow-indigo-950/40 backdrop-blur-sm">
            <img src="/images/Abhipaytech_logo.png" alt="AbhiPay logo" class="w-full rounded-2xl border border-slate-700 bg-slate-100 p-5" />
          </div>
        </div>
      </section>

      <section id="about" class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
        <div class="mb-10 max-w-3xl">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-400">About us</p>
          <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">Built for clarity, speed, and long-term trust.</h2>
        </div>

        <div class="grid gap-8 lg:grid-cols-2">
          <div class="rounded-3xl border border-slate-800 bg-slate-900 p-8">
            <h3 class="text-2xl font-semibold text-white">Our mission</h3>
            <p class="mt-5 text-slate-300">
              We help modern businesses move from manual financial processes to better systems, smarter operations, and more predictable expansion.
            </p>
            <div class="mt-8 space-y-5">
              <div class="flex gap-4">
                <div class="flex h-11 w-11 items-center justify-center rounded-full bg-indigo-500/15 text-lg text-indigo-300">✓</div>
                <div>
                  <p class="font-semibold text-white">Streamlined workflows</p>
                  <p class="mt-1 text-slate-300">Reduce friction and improve turnaround across the payment journey.</p>
                </div>
              </div>
              <div class="flex gap-4">
                <div class="flex h-11 w-11 items-center justify-center rounded-full bg-emerald-500/15 text-lg text-emerald-300">✓</div>
                <div>
                  <p class="font-semibold text-white">Reliable operations</p>
                  <p class="mt-1 text-slate-300">Build confidence with secure and stable infrastructure that scales with you.</p>
                </div>
              </div>
            </div>
          </div>

          <div class="rounded-3xl bg-gradient-to-br from-slate-900 to-slate-800 p-8 ring-1 ring-slate-700">
            <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-300">Why choose us</p>
            <div class="mt-8 space-y-7">
              <div>
                <p class="text-3xl font-black text-white">10+</p>
                <p class="mt-2 text-slate-300">Years of digital finance experience</p>
              </div>
              <div>
                <p class="text-3xl font-black text-white">24/7</p>
                <p class="mt-2 text-slate-300">Dedicated customer support</p>
              </div>
              <div>
                <p class="text-3xl font-black text-white">99.9%</p>
                <p class="mt-2 text-slate-300">Operational reliability</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="financial" class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
        <div class="mb-10 max-w-3xl">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-400">Financial</p>
          <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">Clear financial infrastructure for scalable growth</h2>
        </div>

        <div class="grid gap-6 md:grid-cols-3">
          <div class="rounded-3xl border border-slate-800 bg-slate-900 p-6">
            <p class="text-sm uppercase tracking-[0.2em] text-indigo-300">Payments</p>
            <h3 class="mt-3 text-2xl font-semibold text-white">Faster settlements</h3>
            <p class="mt-3 text-slate-300">Improve transaction speed with secure, efficient payment workflows designed for real business needs.</p>
          </div>
          <div class="rounded-3xl border border-slate-800 bg-slate-900 p-6">
            <p class="text-sm uppercase tracking-[0.2em] text-indigo-300">Cash flow</p>
            <h3 class="mt-3 text-2xl font-semibold text-white">Better visibility</h3>
            <p class="mt-3 text-slate-300">Track movement, forecasting, and treasury insights so teams can plan ahead with more confidence.</p>
          </div>
          <div class="rounded-3xl border border-slate-800 bg-slate-900 p-6">
            <p class="text-sm uppercase tracking-[0.2em] text-indigo-300">Risk</p>
            <h3 class="mt-3 text-2xl font-semibold text-white">Fewer disruptions</h3>
            <p class="mt-3 text-slate-300">Reduce operational risk through stable, compliant, and well-structured financial processes.</p>
          </div>
        </div>
      </section>

      <section id="company-profile" class="mx-auto max-w-7xl px-4 py-20 sm:px-6 lg:px-8">
        <div class="rounded-3xl border border-slate-800 bg-slate-900 p-8 lg:p-10">
          <div class="grid gap-8 lg:grid-cols-[1.1fr_0.9fr]">
            <div>
              <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-400">Company profile</p>
              <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">A growth partner built around trust and execution</h2>
              <p class="mt-5 text-slate-300">
                AbhiPayTech is focused on helping businesses simplify financial operations, improve payment experiences, and build more resilient systems for continuous growth.
              </p>
            </div>

            <div class="grid gap-4 sm:grid-cols-2">
              <div class="rounded-2xl bg-slate-950 p-5">
                <p class="text-sm text-slate-400">Founded</p>
                <p class="mt-2 text-2xl font-bold text-white">2015</p>
              </div>
              <div class="rounded-2xl bg-slate-950 p-5">
                <p class="text-sm text-slate-400">Focus</p>
                <p class="mt-2 text-2xl font-bold text-white">Fintech</p>
              </div>
              <div class="rounded-2xl bg-slate-950 p-5">
                <p class="text-sm text-slate-400">Presence</p>
                <p class="mt-2 text-2xl font-bold text-white">India</p>
              </div>
              <div class="rounded-2xl bg-slate-950 p-5">
                <p class="text-sm text-slate-400">Approach</p>
                <p class="mt-2 text-2xl font-bold text-white">Trusted</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="solutions" class="bg-slate-900/70 py-20">
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
          <div class="mb-12 text-center">
            <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-400">Solutions</p>
            <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">Everything needed to scale smarter</h2>
          </div>

          <div class="grid gap-6 md:grid-cols-3">
            <article v-for="item in solutions" :key="item.title" class="rounded-3xl border border-slate-800 bg-slate-950 p-6 shadow-xl shadow-slate-950/30">
              <div class="mb-5 flex h-14 w-14 items-center justify-center rounded-2xl bg-gradient-to-br text-2xl" :class="item.tone">
                {{ item.icon }}
              </div>
              <h3 class="text-xl font-semibold text-white">{{ item.title }}</h3>
              <p class="mt-3 text-slate-300">{{ item.description }}</p>
            </article>
          </div>
        </div>
      </section>

      <section class="mx-auto max-w-5xl px-4 py-20 sm:px-6 lg:px-8">
        <div class="mb-10 text-center">
          <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-400">FAQ</p>
          <h2 class="mt-4 text-3xl font-bold text-white">Frequently asked questions</h2>
        </div>

        <div class="space-y-4">
          <div v-for="faq in faqs" :key="faq.question" class="rounded-2xl border border-slate-800 bg-slate-900 p-5">
            <p class="font-semibold text-white">{{ faq.question }}</p>
            <p class="mt-2 text-slate-300">{{ faq.answer }}</p>
          </div>
        </div>
      </section>

      <section id="contact" class="mx-auto max-w-7xl px-4 pb-24 pt-8 sm:px-6 lg:px-8">
        <div class="rounded-3xl border border-indigo-500/30 bg-gradient-to-r from-indigo-600/15 to-slate-900 p-8 shadow-2xl shadow-indigo-950/40 lg:p-12">
          <div class="grid gap-8 lg:grid-cols-[1.2fr_0.8fr] lg:items-center">
            <div>
              <p class="text-sm font-semibold uppercase tracking-[0.2em] text-indigo-200">Contact</p>
              <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">Let’s build your next growth milestone.</h2>
              <p class="mt-4 max-w-xl text-slate-200">
                Tell us what you need, and our team will help you create a smarter, faster, and more scalable financial strategy.
              </p>
            </div>

            <div class="rounded-2xl border border-slate-700 bg-slate-950/60 p-5">
              <div class="space-y-4 text-slate-200">
                <p><span class="font-semibold text-white">Email:</span> hello@abhipaytech.com</p>
                <p><span class="font-semibold text-white">Phone:</span> +91 98765 43210</p>
                <p><span class="font-semibold text-white">Address:</span> Pune, Maharashtra, India</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>
