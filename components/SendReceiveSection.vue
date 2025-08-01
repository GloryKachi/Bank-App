<template>
  <section class="py-16 lg:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="flex justify-center mb-28 px-4">
        <h2
            class="w-full max-w-[940px] text-[34px] leading-[37px] tracking-[-0.02em] font-medium text-[#0D2C65] text-center"
        >
          We are on a mission to reduce the cost of sending money to Africa at an average cost of 1%
        </h2>
      </div>



      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-12">

        <!-- (Left Column) -->
        <div>
          <div class="flex items-start space-x-4">
            <div class="flex-1">
              <CurrencyExchange class="hidden md:block" />
            </div>
          </div>
        </div>

        <!-- Receive Money Feature (Right Column) -->
        <div>
          <div class="flex items-start space-x-4">
            <div class="flex-1 ">
              <p class="font-normal text-[24px] leading-[31px] tracking-[-0.02em] text-[#6E80A3] mb-4">
                Why Bomba?
              </p>

              <!-- ONLY mobile-->
              <h3 class="font-medium  tracking-[-0.02em] text-[#0D2C65]
              block  w-full  text-[48px] leading-[56px] align-bottom
">
                Send & Receive money on your own terms
              </h3>
              <div class="block md:hidden mb-6">
                <CurrencyExchange />
              </div>


              <p class="font-normal text-[18px] leading-[26px] tracking-[0em] text-[#6E80A3] mt-10">
                Bomba provides you the luxury of sending money at rates that suit you. You can easily send and swap money between
                <span style="color: #0D2C65;">GBP, USD, NGN</span> and up to 20 other African countries using Bomba’s
                <span style="color: #3ccd7a">'Swap'</span> and
                <span style="color: #3ccd7a">'Express'</span> services. Beat bank rates, save time and gain more.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import CurrencyExchange from "~/components/CurrencyExchange.vue";
</script>
