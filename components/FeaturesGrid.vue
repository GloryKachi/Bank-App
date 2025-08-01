<template>
  <section class="py-10 lg:py-24">
    <div class="flex items-center flex-col justify-center w-full px-4 sm:px-6 lg:px-8">
      <svg class="w-full max-w-[940px] mx-auto" height="2" viewBox="0 0 940 2" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0 1L940 1" stroke="#6E80A3"/>
      </svg>
    </div>

    <!-- Hero Text Section - Made Responsive -->
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center justify-center text-center space-y-4 my-8 sm:my-12 lg:my-16">
      <!-- Mobile-only text -->
      <p class="block md:hidden w-full text-[48px] leading-[56px] tracking-[-0.02em] font-medium align-bottom text-[#0D2C65] text-left">
        The Bomba app is all you need to send money both at home and abroad
      </p>

      <!-- Tablet and Desktop text -->
      <p class="hidden md:block text-2xl sm:text-3xl lg:text-[40px] font-medium leading-tight sm:leading-[1.3] lg:leading-[52px] tracking-[-0.02em] text-[#0D2C65]">
        The Bomba app helps our users send & receive money, swap currencies across borders and pay bills, safely, conveniently, cheaply and on time.
      </p>
      <p class="max-w-4xl text-base sm:text-lg lg:text-[18px] font-normal leading-relaxed lg:leading-[26px] text-[#6E80A3] text-left sm:text-center">
        We are customer-centric and focused on offering values to you that enable you achieve your financial needs.
      </p>

    </div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Features Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 sm:gap-8">

        <!-- First card -->
        <div class="w-full max-w-md mx-auto lg:max-w-none bg-gradient-to-br from-purple-50 to-blue-50 rounded-2xl p-6 sm:p-8 relative overflow-hidden shadow-lg min-h-[450px] sm:min-h-[500px] lg:min-h-[550px]">
          <!-- Heading -->
          <p class="text-xl sm:text-[24px] leading-tight sm:leading-[31px] tracking-tight font-normal font-[PushPenny] text-[#8C8C8C] mb-1">
            Swap
          </p>
          <p class="text-2xl sm:text-[32px] leading-tight sm:leading-[42px] font-bold text-[#0D2C65] mb-3">
            Peer to peer marketplace
          </p>
          <p class="text-base sm:text-[18px] leading-relaxed sm:leading-[26px] text-[#6E80A3] mb-6 pr-4">
            Do you worry about unfavourable exchange rates when sending money? Create or accept offers at your preferred rate on Bomba's Peer to peer marketplace.
          </p>

          <!-- CTA -->
          <div class="flex items-center space-x-3 group cursor-pointer">
            <p class="text-[#1a73e8] font-medium group-hover:underline">
              Swap now
            </p>
            <svg
                width="24"
                height="25"
                viewBox="0 0 24 25"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="group-hover:translate-x-1 transition-transform duration-200"
            >
              <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z"
                  fill="#2668EC"
              />
            </svg>
          </div>

          <!-- Illustration -->
          <div class="absolute bottom-4 right-4">
            <img src="/images/cross.png" alt="Swap illustration" class="w-32 h-32 sm:w-44 sm:h-44 lg:w-56 lg:h-56 object-contain" />
          </div>
        </div>

        <!-- Second card -->
        <div class="w-full max-w-md mx-auto lg:max-w-none bg-[#e6faf5] rounded-2xl p-6 sm:p-8 relative overflow-hidden min-h-[450px] sm:min-h-[500px] lg:min-h-[550px]">
          <p class="text-xl sm:text-[24px] leading-tight sm:leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Express</p>
          <p class="text-2xl sm:text-[32px] leading-tight sm:leading-[42px] font-bold text-[#0D2C65] mb-3 text-left">Take the express lane</p>
          <p class="mb-6 text-[#6E80A3] text-base sm:text-[18px] font-normal leading-relaxed sm:leading-[26px] text-left pr-4">Transact with light speed using Bomba Express. You can send funds at Bomba's exchange rates to family and friends from the UK & US to 20 African countries.</p>

          <div class="flex items-center space-x-3 group cursor-pointer">
            <p class="text-[#1a73e8] text-left font-medium group-hover:underline">
              Send now
            </p>
            <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg" class="group-hover:translate-x-1 transition-transform duration-200">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
            </svg>
          </div>
          <div class="absolute bottom-4 right-4">
            <img src="/images/cash.png" alt="Express illustration" class="w-32 h-32 sm:w-44 sm:h-44 lg:w-52 lg:h-52 object-contain" />
          </div>
        </div>

        <!-- Third card -->
        <div class="w-full max-w-md mx-auto lg:max-w-none bg-[#f0f2f6] rounded-2xl p-6 sm:p-8 relative overflow-hidden min-h-[450px] sm:min-h-[500px] lg:min-h-[550px]">
          <p class="text-xl sm:text-[24px] leading-tight sm:leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Refer & Earn</p>
          <p class="text-2xl sm:text-[32px] leading-tight sm:leading-[42px] font-bold text-[#0D2C65] mb-3 text-left">Make money while you refer</p>
          <p class="mb-6 text-[#6E80A3] text-base sm:text-[18px] font-normal leading-relaxed sm:leading-[26px] text-left pr-4">Bomba allows you to earn passively through its platform. Refer your friends and family to use Bomba and earn up to £140</p>

          <div class="flex items-center space-x-3 group cursor-pointer">
            <p class="text-[#1a73e8] text-left font-medium group-hover:underline">
              Share now
            </p>
            <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg" class="group-hover:translate-x-1 transition-transform duration-200">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
            </svg>
          </div>
          <div class="absolute bottom-4 right-4">
            <img src="/images/gift.png" alt="Refer illustration" class="w-32 h-32 sm:w-48 sm:h-48 lg:w-64 lg:h-64 object-contain" />
          </div>
        </div>

        <!-- Fourth card -->
        <div class="w-full max-w-md mx-auto lg:max-w-none bg-[#fdf3ef] rounded-2xl p-6 sm:p-8 relative overflow-hidden min-h-[450px] sm:min-h-[500px] lg:min-h-[550px]">
          <p class="text-xl sm:text-[24px] leading-tight sm:leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Bomba Connect</p>
          <p class="text-2xl sm:text-[32px] leading-tight sm:leading-[42px] font-bold text-[#0D2C65] mb-3 text-left">Deals from top brands</p>
          <p class="mb-6 text-[#6E80A3] text-base sm:text-[18px] font-normal leading-relaxed sm:leading-[26px] text-left pr-4">With Bomba Connect, you can pay for and access goods and services from some of the best and trusted brands - at the best rates and with minimal wait time - all within the Bomba App.</p>

          <div class="flex items-center space-x-3 group cursor-pointer">
            <p class="text-[#1a73e8] text-left font-medium group-hover:underline">
              Explore now
            </p>
            <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg" class="group-hover:translate-x-1 transition-transform duration-200">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
            </svg>
          </div>
          <div class="absolute bottom-4 right-4">
            <img src="/images/cart.png" alt="Connect illustration" class="w-32 h-32 sm:w-48 sm:h-48 lg:w-64 lg:h-64 object-contain" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Methods
const handleSwapNow = () => {
  console.log('Navigating to swap marketplace...')
  // Handle navigation to P2P marketplace
  // You could use navigateTo('/swap') or similar
}
</script>

<style scoped>
.perspective-1000 {
  perspective: 1000px;
}

.rotate-x-45 {
  transform: rotateX(45deg);
}
</style>