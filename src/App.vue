<template>
  <div class="bg-white">
    <!-- Header -->
    <header class="absolute inset-x-0 top-0 z-50">
      <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Worklog Assistant</span>
            <img class="h-8 w-auto" src="/src/assets/logo.ico" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation" :key="item.name" :href="item.href"
            class="text-sm font-semibold leading-6 text-gray-900">{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <!-- <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Log in <span
              aria-hidden="true">&rarr;</span></a> -->
        </div>
      </nav>
      <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel
          class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Your Company</span>
              <img class="h-8 w-auto" src="/src/assets/logo.ico" alt="" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation" :key="item.name" :href="item.href"
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">{{
                    item.name }}</a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>

    <main class="isolate">
      <!-- Hero section -->
      <div class="relative pt-14">
        <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
          aria-hidden="true">
          <div
            class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
            style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
        </div>
        <div class="py-24 sm:py-32">
          <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl text-center">
              <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">JIRA Time Tracking without the
                pain</h1>
              <p class="mt-6 text-lg leading-8 text-gray-600">
                Stop logging work manually. Track your work as you do with the easy desktop app and ensure accuracy
              </p>
              <div class="mt-10 flex items-center justify-center gap-x-6">
                <a href="public/WorklogAssistant-windows-0.0.5.zip"
                  class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
                  Get started
                </a>
                <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Learn more<span
                    aria-hidden="true">→</span></a>
              </div>
            </div>
            <div class="mt-16 flow-root sm:mt-24">
              <div
                class="-m-2 rounded-xl bg-gray-900/5 p-2 ring-1 ring-inset ring-gray-900/10 lg:-m-4 lg:rounded-2xl lg:p-4">
                <img src="/src/assets/big.png" alt="App screenshot" width="2432" height="1442"
                  class="rounded-md shadow-2xl ring-1 ring-gray-900/10" />
              </div>
            </div>
          </div>
        </div>
        <div
          class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
          aria-hidden="true">
          <div
            class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
            style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
        </div>
      </div>

      <!-- Feature section -->
      <div class="mx-auto mt-4 max-w-7xl px-6 sm:mt-4 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <h2 class="text-base font-semibold leading-7 text-indigo-600">Track more accurately
          </h2>
          <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Easy JIRA integration for
            immediate accurate time tracking
          </p>
          <p class="mt-6 text-lg leading-8 text-gray-600">Don't waste time manually recording what you did - save time
            with the Worklog Assistant Desktop app
          </p>
        </div>
        <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
          <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
            <div v-for="feature in features" :key="feature.name" class="relative pl-16">
              <dt class="text-base font-semibold leading-7 text-gray-900">
                <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                  <component :is="feature.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                </div>
                {{ feature.name }}
              </dt>
              <dd class="mt-2 text-base leading-7 text-gray-600">{{ feature.description }}</dd>
            </div>
          </dl>
        </div>
      </div>

      <!-- Pricing section -->
      <div class="py-24 sm:pt-48">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div class="mx-auto max-w-4xl text-center">
            <h2 class="text-base font-semibold leading-7 text-indigo-600">Pricing</h2>
            <p class="mt-2 text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl">
              Pricing plans for teams or businesses
            </p>
          </div>
          <!-- <p class="mx-auto mt-6 max-w-2xl text-center text-lg leading-8 text-gray-600">Distinctio et nulla eum soluta
            et neque labore quibusdam. Saepe et quasi iusto modi velit ut non voluptas in. Explicabo id ut laborum.</p> -->
          <div
            class="isolate mx-auto mt-16 grid max-w-md grid-cols-1 gap-y-8 sm:mt-20 lg:mx-0 lg:max-w-none lg:grid-cols-3">
            <div v-for="(tier, tierIdx) in tiers" :key="tier.id"
              :class="[tier.mostPopular ? 'lg:z-10 lg:rounded-b-none' : 'lg:mt-8', tierIdx === 0 ? 'lg:rounded-r-none' : '', tierIdx === tiers.length - 1 ? 'lg:rounded-l-none' : '', 'flex flex-col justify-between rounded-3xl bg-white p-8 ring-1 ring-gray-200 xl:p-10']">
              <div>
                <div class="flex items-center justify-between gap-x-4">
                  <h3 :id="tier.id"
                    :class="[tier.mostPopular ? 'text-indigo-600' : 'text-gray-900', 'text-lg font-semibold leading-8']">
                    {{ tier.name }}</h3>
                  <p v-if="tier.mostPopular"
                    class="rounded-full bg-indigo-600/10 px-2.5 py-1 text-xs font-semibold leading-5 text-indigo-600">
                    Most popular</p>
                </div>
                <p class="mt-4 text-sm leading-6 text-gray-600">{{ tier.description }}</p>
                <p class="mt-6 flex items-baseline gap-x-1">
                  <span class="text-4xl font-bold tracking-tight text-gray-900">{{ tier.priceMonthly }}</span>
                  <span class="text-sm font-semibold leading-6 text-gray-600">/month</span>
                </p>
                <ul role="list" class="mt-8 space-y-3 text-sm leading-6 text-gray-600">
                  <li v-for="feature in tier.features" :key="feature" class="flex gap-x-3">
                    <CheckIcon class="h-6 w-5 flex-none text-indigo-600" aria-hidden="true" />
                    {{ feature }}
                  </li>
                </ul>
              </div>
              <a :href="tier.href" :aria-describedby="tier.id"
                :class="[tier.mostPopular ? 'bg-indigo-600 text-white shadow-sm hover:bg-indigo-500' : 'text-indigo-600 ring-1 ring-inset ring-indigo-200 hover:ring-indigo-300', 'mt-8 block rounded-md px-3 py-2 text-center text-sm font-semibold leading-6 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600']">Buy
                plan</a>
            </div>
          </div>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <div class="mx-auto mt-4 max-w-7xl px-6 lg:px-8">
      <footer aria-labelledby="footer-heading" class="relative border-t border-gray-900/10 py-24 sm:mt-56 sm:py-32">
        <h2 id="footer-heading" class="sr-only">Footer</h2>
        <div class="xl:grid xl:grid-cols-3 xl:gap-8">
          <img class="h-7" src="/src/assets/logo.ico" alt="Worklog Assistant" /> Worklog Assistant
          <!-- <div class="mt-16 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold leading-6 text-gray-900">Solutions</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.solutions" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-600 hover:text-gray-900">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold leading-6 text-gray-900">Support</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.support" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-600 hover:text-gray-900">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold leading-6 text-gray-900">Company</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.company" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-600 hover:text-gray-900">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold leading-6 text-gray-900">Legal</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.legal" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-600 hover:text-gray-900">{{ item.name }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </div> -->
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import {
  ArrowPathIcon,
  Bars3Icon,
  CloudArrowUpIcon,
  FingerPrintIcon,
  LockClosedIcon,
  XMarkIcon,
} from '@heroicons/vue/24/outline'
import { CheckIcon } from '@heroicons/vue/20/solid'

const navigation = [
  { name: 'Product', href: '/' },
  // { name: 'Features', href: '#' },
  // { name: 'Marketplace', href: '#' },
  // { name: 'Company', href: '#' },
]
const features = [
  {
    name: 'One click work logging',
    description:
      'Bulk upload all the daily or weekly worklogs',
    icon: CloudArrowUpIcon,
  },
  {
    name: 'Accurate tracking',
    description:
      'Review and amend draft worklogs before upload',
    icon: CloudArrowUpIcon,
  },
  {
    name: 'Easy Install',
    description:
      'Use our enterprise options, or simply download and run without needing an IT team to install',
    icon: ArrowPathIcon,
  },
  {
    name: 'Simple security',
    description:
      'Your data never leaves your PC - security by default',
    icon: FingerPrintIcon,
  },
]
const tiers = [
  {
    name: 'Personal',
    id: 'tier-personal',
    href: '#',
    priceMonthly: '$10',
    description: 'A single license for yourself, get started in 5 minutes',
    features: ['Unlimited projects', 'Unlimited tracking', 'Simple worklogs', '24 - hour support response time', '1 license just for yourself'],
    mostPopular: true,
  },
  {
    name: 'Enterprise',
    id: 'tier-enterprise',
    href: '#',
    priceMonthly: '$12',
    description: 'A plan that scales with your rapidly growing business.',
    features: ['Unlimited projects', 'Unlimited tracking', 'Simple worklogs', '24 - hour support response time', 'Licenses for everybody in your organisation, plus onboarding support and custom deployment setup'],
    mostPopular: false,
  },
]
const faqs = [

]
const footerNavigation = {
  // solutions: [
  //   { name: 'Hosting', href: '#' },
  //   { name: 'Data Services', href: '#' },
  //   { name: 'Uptime Monitoring', href: '#' },
  //   { name: 'Enterprise Services', href: '#' },
  // ],
  // support: [
  //   { name: 'Pricing', href: '#' },
  //   { name: 'Documentation', href: '#' },
  //   { name: 'Guides', href: '#' },
  //   { name: 'API Reference', href: '#' },
  // ],
  // company: [
  //   { name: 'About', href: '#' },
  //   { name: 'Blog', href: '#' },
  //   { name: 'Jobs', href: '#' },
  //   { name: 'Press', href: '#' },
  //   { name: 'Partners', href: '#' },
  // ],
  // legal: [
  //   { name: 'Claim', href: '#' },
  //   { name: 'Privacy', href: '#' },
  //   { name: 'Terms', href: '#' },
  // ],
}

const mobileMenuOpen = ref(false)
</script>