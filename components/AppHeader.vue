<!--<template>-->
<!--  <header-->
<!--      class="bg-white  border-b border-b-gray-400 shadow-sm"-->
<!--      style="border-top-style: dashed; border-bottom-style: solid;"-->
<!--  >-->
<!--    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">-->
<!--      <div class="flex justify-center items-center h-16 relative">-->

<!--        &lt;!&ndash; Navigation Links &ndash;&gt;-->
<!--        <div class="hidden md:block">-->
<!--          <div class="flex items-center space-x-8">-->
<!--            <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">-->
<!--              Features-->
<!--              <svg class="w-4 h-4 ml-1 text-[#63C57B]" fill="none" stroke="currentColor" viewBox="0 0 24 24">-->
<!--                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />-->
<!--              </svg>-->
<!--            </a>-->
<!--            <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">-->
<!--              Press-->
<!--            </a>-->
<!--            <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">-->
<!--              Company-->
<!--              <svg class="w-4 h-4 ml-1 text-[#63C57B]" fill="none" stroke="currentColor" viewBox="0 0 24 24">-->
<!--                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />-->
<!--              </svg>-->

<!--            </a>-->
<!--          </div>-->
<!--        </div>-->

<!--        &lt;!&ndash; Mobile menu button &ndash;&gt;-->
<!--        <div class="absolute right-0 md:hidden">-->
<!--          <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-900 hover:text-blue-800 p-2">-->
<!--            <svg width="48" height="15" viewBox="0 0 48 15" fill="none" xmlns="http://www.w3.org/2000/svg">-->
<!--              <path d="M46.4771 1.51758H2.04688" stroke="#233375" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>-->
<!--              <path d="M46.4771 13.6777H2.04688" stroke="#233375" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>-->
<!--            </svg>-->

<!--          </button>-->
<!--        </div>-->
<!--      </div>-->

<!--      &lt;!&ndash; Mobile menu &ndash;&gt;-->
<!--      <div v-show="mobileMenuOpen" class="md:hidden">-->
<!--        <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-white border-t border-dashed">-->
<!--          <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">-->
<!--            Features-->
<!--            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">-->
<!--              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />-->
<!--            </svg>-->
<!--          </a>-->
<!--          <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">-->
<!--            Press-->
<!--            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">-->
<!--              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />-->
<!--            </svg>-->
<!--          </a>-->
<!--          <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">-->
<!--            Company-->
<!--            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">-->
<!--              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />-->
<!--            </svg>-->
<!--          </a>-->
<!--        </div>-->
<!--      </div>-->
<!--    </nav>-->
<!--  </header>-->
<!--</template>-->

<!--<script setup>-->
<!--import { ref } from 'vue'-->

<!--const mobileMenuOpen = ref(false)-->
<!--</script>-->


<template>
  <div>
    <!-- Fixed Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white border-b border-b-gray-400 shadow-sm" style="border-top-style: dashed; border-bottom-style: solid;">
      <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-center items-center h-16 relative">
          <!-- Navigation Links -->
          <div class="hidden md:block">
            <div class="flex items-center space-x-8">
              <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">
                Features
                <svg class="w-4 h-4 ml-1 text-[#63C57B]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </a>
              <NuxtLink to="/blog" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">
                Press
              </NuxtLink>
              <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 px-3 py-2 text-sm font-medium transition-colors">
                Company
                <svg class="w-4 h-4 ml-1 text-[#63C57B]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </a>
            </div>
          </div>

          <!-- Mobile menu button -->
          <div class="absolute right-0 md:hidden">
            <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-900 hover:text-blue-800 p-2">
              <svg width="48" height="15" viewBox="0 0 48 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M46.4771 1.51758H2.04688" stroke="#233375" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M46.4771 13.6777H2.04688" stroke="#233375" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </button>
          </div>
        </div>

        <!-- Mobile menu -->
        <div v-show="mobileMenuOpen" class="md:hidden absolute top-full left-0 right-0 bg-white border-t border-dashed shadow-lg">
          <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
            <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">
              Features
              <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </a>
            <NuxtLink to="/blog" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">
              Press
            </NuxtLink>
            <a href="#" class="flex items-center text-gray-900 hover:text-blue-800 block px-3 py-2 text-base font-medium">
              Company
              <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </a>
          </div>
        </div>
      </nav>
    </header>

    <!-- Main content starts right after the fixed header -->
    <main class="">
      <!-- Your page content goes here -->
      <div class="max-w-md mx-auto bg-white p-6 space-y-6">
        <!-- This is where your other components will render -->
        <slot />
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const mobileMenuOpen = ref(false)
</script>

