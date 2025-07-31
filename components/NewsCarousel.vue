<template>
  <div class="w-full py-10 px-4 md:px-10">
      <div class="relative overflow-hidden min-h-[220px] md:min-h-[180px]">
        <transition name="fade-slide" mode="out-in">
          <div
              :key="currentSlideIndex"
              class="absolute top-0 left-0 w-full flex flex-col md:flex-row justify-between gap-6 transition-all duration-700 ease-in-out"
          >
            <!-- Left-->
            <div class="flex-1 text-left">
              <h2 class="font-medium w-[703px] md:text-3xl  text-[#0D2C65]" style="font-size: 64px; line-height: 77px; letter-spacing: -0.02em;">
                {{ slides[currentSlideIndex].title }}
              </h2>
            </div>

            <!-- Right: News Items -->
            <div class="flex-1 w-full">
              <p class=" text-left pt-20 w-full" style="font-weight: 400; font-size: 18px; line-height: 26px; vertical-align: bottom; color: #233375;">
                {{ slides[currentSlideIndex].paragraph }}
              </p>
            </div>

          </div>
        </transition>
      </div>
    </div>

    <div class="flex items-center justify-between w-full max-w-3xl mx-auto mb-10">
      <template v-for="(slide, index) in slides" :key="index">
        <div
            class="flex items-center text-white relative cursor-pointer group"
            @click="currentSlideIndex = index"
        >


          <div
              v-if="index !== slides.length - 1"
              class="absolute top-1/2 left-full h-0.5 w-24 transform -translate-y-1/2 translate-x-2 bg-blue-300 z-0 group-hover:bg-blue-400 transition-all duration-300"
              :class="{'bg-blue-600': index < currentSlideIndex}"
          ></div>


        </div>
      </template>
    </div>

  <div class="bg-[#f8f9ff] py-6 px-4 md:px-10 w-full">
    <div class="flex flex-col md:flex-row md:items-center justify-between w-full">


      <div class="flex flex-col md:flex-row md:items-center md:gap-6">
        <!-- Left Column -->
        <p class="font-medium  md:mb-0 text-[#6E80A3] pb-8" style="font-weight: 400; font-size: 15px; line-height: 24px">
          News & Release update
        </p>

        <!-- Middle Column -->
        <div class="text-sm text-gray-700 space-y-1 text-left">
          <p>
            <span class="text-[#6E80A3]" style="font-size: 17px; line-height: 27px; font-weight: 400">June 20, 2022 — </span>
            <a href="#" class="text-[#2668EC] hover:underline" style="font-size: 17px; line-height: 27px; font-weight: 400">Bomba now has a dollar wallet, activate your account</a>
          </p>
          <p>
            <span class="text-[#6E80A3]" style="font-size: 17px; line-height: 27px; font-weight: 400">June 01, 2022 — </span>
            <a href="#" class="text-[#2668EC] hover:underline" style="font-size: 17px; line-height: 27px; font-weight: 400">Top 10 Summer Vacation Places In 2022</a>
          </p>
        </div>
      </div>

      <!-- Right Column -->
      <div class="mt-4 md:mt-0 text-sm font-medium text-[#233375] flex items-center gap-1 whitespace-nowrap" style="font-size: 24px; line-height: 31px; font-weight: 400">
        Scroll Down <span class="text-green-500 text-lg" style="font-size: 24px">↓</span>
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
    title: 'Make instant transfers \n' +
        'with Express',
    paragraph: 'When you send money using \'Express\' - it’s sent at Bomba exchange rate and your transaction is completed instantly',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  },
  {
    title: 'Review and confirm \n' +
        'your transaction ',
    paragraph: 'Review your transaction, ensure that the provided details are correct, then click the send button!  ',
    news: [
      { date: 'July 5', text: 'Live in Beta', link: '#' },
      { date: 'July 6', text: 'Official Launch', link: '#' }
    ]
  },
  {
    title: 'Completed! \n' +
        'Fast, easy and secure ',
    paragraph: 'Money on its way! Send money today to your friends, family or make payment to a business.  Get started → ',
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
