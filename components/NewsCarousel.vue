<template>
  <div class="w-full py-6 sm:py-8 lg:py-10 px-4 sm:px-6 lg:px-10">
    <div class="relative overflow-hidden min-h-[400px] sm:min-h-[350px] lg:min-h-[220px]">
      <transition name="fade-slide" mode="out-in">
        <div
            :key="currentSlideIndex"
            class="absolute top-0 left-0 w-full flex flex-col lg:flex-row justify-between gap-4 sm:gap-6 transition-all duration-700 ease-in-out"
        >
          <!-- Left-->
          <div class="flex-1 text-left">
            <h2 class="font-medium w-full max-w-full lg:max-w-[703px] text-4xl sm:text-5xl lg:text-4xl xl:text-[64px] text-[#0D2C65] leading-tight sm:leading-[1.1] xl:leading-[77px] tracking-[-0.02em]">
              {{ slides[currentSlideIndex].title }}
            </h2>
          </div>

          <!-- Right: News Items -->
          <div class="flex-1 w-full">
            <p class="text-left pt-6 sm:pt-8 lg:pt-20 w-full text-lg sm:text-xl lg:text-[18px] font-normal leading-relaxed lg:leading-[26px] text-[#233375]">
              {{ slides[currentSlideIndex].paragraph }}
            </p>

            <!-- Play Button - Mobile Only -->
            <div class="mt-6 lg:hidden">
              <div class="flex items-center gap-3 mb-4">
                <button class="flex items-center justify-center w-12 h-12 bg-[#0D2C65] rounded-full text-white hover:bg-[#1a3a7a] transition-colors">
                  <img src="/images/play-icon.svg" alt="Play" class="w-4 h-4" />
                </button>
                <p class="text-sm text-[#0D2C65] font-medium">See how it works</p>
              </div>

              <!-- Green arrow directly below play button -->
              <div class="flex justify-start px-4">
                <img src="/images/arrow-down.svg" alt="">
<!--                <span class="text-green-500 text-2xl text-center">↓</span>-->
              </div>
            </div>
          </div>
        </div>
      </transition>
    </div>
  </div>

  <div class="flex items-center justify-between w-full max-w-3xl mx-auto mb-6 sm:mb-8 lg:mb-10 px-4">
    <template v-for="(slide, index) in slides" :key="index">
      <div
          class="flex items-center text-white relative cursor-pointer group"
          @click="currentSlideIndex = index"
      >
        <div
            v-if="index !== slides.length - 1"
            class="absolute top-1/2 left-full h-0.5 w-16 sm:w-20 lg:w-24 transform -translate-y-1/2 translate-x-2 bg-blue-300 z-0 group-hover:bg-blue-400 transition-all duration-300"
            :class="{'bg-blue-600': index < currentSlideIndex}"
        ></div>
      </div>
    </template>
  </div>

  <div class=" hidden md:block bg-[#f8f9ff] py-4 sm:py-6 px-4 sm:px-6 lg:px-10 w-full">
    <div class="flex flex-col lg:flex-row lg:items-center justify-between w-full gap-4 lg:gap-0">
      <div class="flex flex-col lg:flex-row lg:items-center lg:gap-6">
        <!-- Left Column -->
        <p class="font-normal text-sm sm:text-[15px] leading-relaxed lg:leading-[24px] text-[#6E80A3] mb-4 lg:mb-0">
          News & Release update
        </p>

        <!-- Middle Column -->
        <div class="text-sm text-gray-700 space-y-2 sm:space-y-1 text-left">
          <p class="flex flex-col sm:flex-row sm:items-start gap-1 sm:gap-0">
            <span class="text-[#6E80A3] text-base sm:text-[17px] leading-relaxed sm:leading-[27px] font-normal">June 20, 2022 — </span>
            <a href="#" class="text-[#2668EC] hover:underline text-base sm:text-[17px] leading-relaxed sm:leading-[27px] font-normal">Bomba now has a dollar wallet, activate your account</a>
          </p>
          <p class="flex flex-col sm:flex-row sm:items-start gap-1 sm:gap-0">
            <span class="text-[#6E80A3] text-base sm:text-[17px] leading-relaxed sm:leading-[27px] font-normal">June 01, 2022 — </span>
            <a href="#" class="text-[#2668EC] hover:underline text-base sm:text-[17px] leading-relaxed sm:leading-[27px] font-normal">Top 10 Summer Vacation Places In 2022</a>
          </p>
        </div>
      </div>

      <!-- Right Column -->
      <div class="mt-2 lg:mt-0 text-lg sm:text-xl lg:text-[24px] font-normal leading-tight lg:leading-[31px] text-[#233375] lg:flex lg:items-center lg:gap-1 lg:whitespace-nowrap hidden lg:block">
        Scroll Down
        <!-- Desktop: Original text arrow -->
        <span class="text-green-500 text-xl sm:text-2xl lg:text-[24px]">↓</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

interface Slide {
  title: string
  paragraph: string
  news: { date: string; text: string; link: string }[]
}

const slides = ref<Slide[]>([
  {
    title: 'Multi-currency accounts for Africans',
    paragraph: 'Transact at home and abroad - create, send, hold and receive money in African and foreign currencies. Send money to and from Africa, seamlessly.',
    news: [
      { date: 'July 1', text: 'Initial Release', link: '#' },
      { date: 'July 2', text: 'Added Stepper UI', link: '#' }
    ]
  },
  {
    title: 'Choose from several payment methods',
    paragraph: 'With Bomba, you get to choose how you send and receive money; send at your own rate with \'Swap\', send and receive instantly with \'Express\',  or make free local transfers with \'Withdraw Money\'',
    news: [
      { date: 'July 3', text: 'Improved UX', link: '#' },
      { date: 'July 4', text: 'Added Animation', link: '#' }
    ]
  },
  {
    title: 'Accept and create offers with Swap',
    paragraph: 'You can send money internationally at your preferred rate on our Peer-to-peer Marketplace by choosing or accepting an offer. Created offers get accepted within an average time of 30 minutes',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  },
  {
    title: 'Make instant transfers with Express',
    paragraph: 'When you send money using \'Express\' - it\'s sent at Bomba exchange rate and your transaction is completed instantly',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  },
  {
    title: 'Review and confirm your transaction',
    paragraph: 'Review your transaction, ensure that the provided details are correct, then click the send button!',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  },
  {
    title: 'Completed! Fast, easy and secure',
    paragraph: 'Money on its way! Send money today to your friends, family or make payment to a business. Get started →',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  }
])

const currentSlideIndex = ref<number>(0)
let intervalId: number

onMounted(() => {
  intervalId = setInterval(() => {
    currentSlideIndex.value = (currentSlideIndex.value + 1) % slides.value.length
  }, 5000)
})

onUnmounted(() => {
  clearInterval(intervalId)
})
</script>

<style scoped>
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: opacity 0.6s ease, transform 0.6s ease;
}
.fade-slide-enter-from {
  opacity: 0;
  transform: translateX(50%);
}
.fade-slide-leave-to {
  opacity: 0;
  transform: translateX(-50%);
}
</style>