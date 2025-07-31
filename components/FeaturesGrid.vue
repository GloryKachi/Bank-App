<template>
  <section class="py-10 lg:py-24 ">
    <div class="flex items-center flex-col justify-center w-full">
      <svg class="w-full max-w-[940px] mx-auto" height="2" viewBox="0 0 940 2" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0 1L940 1" stroke="#6E80A3"/>
      </svg>
    </div>

    <div class="w-[1047.96px] h-[176.43px] mx-auto flex flex-col items-center justify-center text-center space-y-4 my-16">
      <p class="text-[40px] font-medium leading-[52px] tracking-[-0.02em] text-[#0D2C65]">
        The Bomba app helps our users send & receive money, swap currencies across borders and pay bills, safely, conveniently, cheaply and on time.
      </p>
      <p class=" w-[712px] text-[18px] font-normal leading-[26px] text-[#6E80A3]">
        We are customer-centric and focused on offering values to you that enable you achieve your financial needs.
      </p>
    </div>



    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">

<!--        first card-->
        <div class="max-w-md min-h-[550px] mx-auto bg-gradient-to-br from-purple-50 to-blue-50 rounded-2xl p-8 relative overflow-hidden shadow-lg">
          <!-- Heading -->
          <p class="text-[24px] leading-[31px] tracking-tight font-normal font-[PushPenny] text-[#8C8C8C] mb-1">
            Swap
          </p>
          <p class="text-[32px] leading-[42px] font-bold text-[#0D2C65] mb-3">
            Peer to peer marketplace
          </p>
          <p class="max-w-[415px] text-[18px] leading-[26px] text-[#6E80A3] mb-6">
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
            <img src="/images/cross.png" alt="Swap illustration" class="w-56 h-56 object-contain" />
          </div>
        </div>


<!--        second card-->

        <div class="max-w-md min-h-[550px] mx-auto bg-[#e6faf5] from-purple-50 to-blue-50 rounded-2xl p-8 relative overflow-hidden" >
          <!-- Image from public folder -->

          <p class="text-[24px] leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Express</p>
          <p class="text-lg font-semibold mb-3 text-[#0D2C65] text-left " style="font-weight: 700; line-height: 42px; font-size: 32px">Take the express lane</p>
          <p class="mb-6 text-[#6E80A3] text-[18px] font-normal leading-[26px] text-left w-[415.69px]">Transact with light speed using Bomba Express. You can send funds at Bomba’s exchange rates to family and friends from the UK & US to 20 African countries.</p>

          <div class="flex items-center">
            <p class="text-[#1a73e8] text-left  py-2  font-medium">
              Send now
            </p>
            <div class="mx-5">
              <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
              </svg>

            </div>
          </div>
          <div class="absolute bottom-4 right-4">
            <img src="/images/cash.png" alt="Swap illustration" class="w-52 h-52 object-contain" />
          </div>
        </div>

<!--        third card-->

        <div class="max-w-md min-h-[550px] mx-auto bg-[#f0f2f6] from-purple-50 to-blue-50 rounded-2xl p-8 relative overflow-hidden" >
          <!-- Image from public folder -->

          <p class="text-[24px] leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Refer & Earn</p>
          <p class="text-lg font-semibold mb-3 text-[#0D2C65] text-left " style="font-weight: 700; line-height: 42px; font-size: 32px">Make money while you refer</p>
          <p class="mb-6 text-[#6E80A3] text-[18px] font-normal leading-[26px] text-left w-[415.69px]">Bomba allows you to earn passively through its platform. Refer your friends and family to use Bomba and earn up to £140</p>

          <div class="flex items-center">
            <p class="text-[#1a73e8] text-left  py-2  font-medium">
              Share now
            </p>
            <div class="mx-5">
              <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
              </svg>

            </div>
          </div>
          <div class=" absolute bottom-4 right-4">
            <img src="/images/gift.png" alt="Swap illustration" class="w-64 h-64 object-contain" />
          </div>
        </div>

<!--        fourth card-->

        <div class="max-w-md m-h-[550px] mx-auto bg-[#fdf3ef] from-purple-50 to-blue-50 rounded-2xl p-8 relative overflow-hidden" >
          <!-- Image from public folder -->

          <p class="text-[24px] leading-[31px] tracking-[-0.02em] font-[400] font-[PushPenny] text-[#8C8C8C] text-left">Bomba Connect</p>
          <p class="text-lg font-semibold mb-3 text-[#0D2C65] text-left " style="font-weight: 700; line-height: 42px; font-size: 32px">Deals from top brands</p>
          <p class="mb-6 text-[#6E80A3] text-[18px] font-normal leading-[26px] text-left w-[415.69px]">With Bomba Connect, you can pay for and access goods and services from some of the best and trusted brands - at the best rates and with minimal wait time - all within the Bomba App.</p>

          <div class="flex items-center">
            <p class="text-[#1a73e8] text-left  py-2  font-medium">
              Explore now
            </p>
            <div class="mx-5">
              <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M18.5303 13.2735C18.8232 12.9806 18.8232 12.5057 18.5303 12.2128L14.5303 8.21283C14.2374 7.91994 13.7626 7.91994 13.4697 8.21283C13.1768 8.50573 13.1768 8.9806 13.4697 9.27349L16.1893 11.9932H6C5.58579 11.9932 5.25 12.329 5.25 12.7432C5.25 13.1574 5.58579 13.4932 6 13.4932H16.1893L13.4697 16.2128C13.1768 16.5057 13.1768 16.9806 13.4697 17.2735C13.7626 17.5664 14.2374 17.5664 14.5303 17.2735L18.5303 13.2735Z" fill="#2668EC"/>
              </svg>

            </div>
          </div>
          <div class="absolute bottom-4 right-4">
            <img src="/images/cart.png" alt="Swap illustration" class="h-64 w-64 object-contain" />
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