<template>
  <footer class="bg-gray-50 py-16 px-6">
    <div class="max-w-6xl mx-auto">
      <!-- Main CTA Section -->
      <h2 class="w-full text-[48px] md:text-5xl font-medium text-[#0D2C65] mb-3 text-left leading-[56px] md:leading-[74px] tracking-[-0.02em]">
        Sign up for free
      </h2>
      <p class="w-full text-[48px] mb-10 md:text-5xl font-medium text-[#0D2C65] text-left leading-[56px] md:leading-[74px] tracking-[-0.02em]">
        Join thousands of users
      </p>


      <!-- Footer Links Grid -->
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
        <!-- Company Column -->
        <div>
          <p class="text-[16px] font-medium text-[#0D2C65] tracking-wider leading-[18px] mb-4">
            Company
          </p>
          <ul class="space-y-3">
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">About Us</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">Features</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">Blog</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">Careers</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">Legal</a></li>
          </ul>
        </div>

        <!-- Support Column -->
        <div>
          <h3 class="text-[16px] font-medium text-[#0D2C65] tracking-wider leading-[18px]  mb-4">
            Support
          </h3>
          <ul class="space-y-3">
            <li><a href="mailto:hello@bomba.co" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">hello@bomba.co</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">WhatsApp ↗</a></li>
            <li><a href="#" class="text-[#6E80A3] text-[24px] leading-[31px] font-normal hover:text-blue-800 transition-colors">Help Center</a></li>
          </ul>
        </div>


        <div></div>

        <!-- Company Info Column -->
        <div>
          <p class="w-[280px] text-[18px] font-normal text-[#0D2C65] leading-[26px] mb-2">
            The neo bank for Africans globally
          </p>
          <p class="font-normal w-[401px] py-[7px] text-[#6E80A3] text-[18px] leading-[26px]">
            Bomba Ltd is a UK-incorporated Company with Registration Number: (RC: 1252577)
          </p>

        </div>
      </div>

      <!-- Newsletter Section -->


      <!-- App Store Buttons -->
      <div class="parent flex flex-col md:flex-row justify-between gap-12 mt-40 px-4">
        <!-- Left Section: App Stores + Footer Links -->
        <div class="flex-1">
          <!-- App Store Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 mb-12">
            <a href="#" class="inline-block">
              <img src="/images/Google%20Store.png" class="w-[186px]" alt="Google play" />
            </a>
            <a href="#" class="inline-block">
              <img src="/images/App%20Store.png" class="w-[186px]" alt="App store" />
            </a>
          </div>

          <!-- Footer Links -->
          <div class="border-t border-gray-200 pt-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center space-y-4 md:space-y-0">
              <div class="text-sm text-gray-500">
                <p>© 2022 Bomba Limited. All rights reserved.</p>
                <div class="flex flex-wrap gap-4 mt-2">
                  <a href="#" class="text-blue-600 hover:text-blue-800 transition-colors">Terms of Service</a>
                  <a href="#" class="text-blue-600 hover:text-blue-800 transition-colors">Privacy Policy</a>
                  <a href="#" class="text-blue-600 hover:text-blue-800 transition-colors">TBC/UV</a>
                  <a href="#" class="text-blue-600 hover:text-blue-800 transition-colors">Cookie Policy</a>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Section: Newsletter -->

        <div class="flex-1 max-w-md">
          <p class="text-sm font-medium text-gray-600 mb-4">
            Stay updated on our newsletter
          </p>

          <!-- Newsletter -->
          <div class="flex flex-col sm:flex-row gap-3">
            <input
                v-model="email"
                type="email"
                placeholder="Enter your email address"
                class="flex-1 px-4 py-3 bg-[#233375] text-[#6E80A3] rounded-lg border-0 focus:ring-2 focus:ring-indigo-600 focus:outline-none"
            />
            <button
                @click="handleSubscribe"
                class="px-6 py-3 bg-transparent text-[14px] leading-[26px] text-[#2668EC] rounded-lg hover:bg-blue-600 hover:text-white transition-colors font-medium"
            >
              Subscribe &gt;
            </button>
          </div>

          <!-- Social Links -->
          <div class="mt-6 text-right text-[15px] leading-[24px] tracking-normal font-normal text-[#6E80A3] font-[PushPenny]">
            <div class="flex gap-16">
              <a href="#" class="hover:underline">Instagram</a>
              <a href="#" class="hover:underline">Facebook</a>
              <a href="#" class="hover:underline">LinkedIn</a>
              <a href="#" class="hover:underline">Twitter</a>
            </div>
          </div>
        </div>

      </div>



    </div>
  </footer>
</template>

<script setup>
// Reactive data
const email = ref('')

// Methods
const handleSubscribe = () => {
  if (email.value) {
    console.log('Subscribing email:', email.value)
    email.value = ''
  }
}
</script>

<style scoped>
</style>