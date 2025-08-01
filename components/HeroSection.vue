<template>
  <section class="bg-light-gray py-8 sm:py-16 lg:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="flex flex-col items-center justify-center gap-8 sm:gap-12 text-center">

        <div class="flex justify-center w-full">
          <!-- Mobile only-->
          <img
              src="/images/mobile-phone.png"
              alt="Mobile Phone Display"
              class="w-full mt-14 max-w-[280px]  object-cover sm:hidden"
          />

          <!-- Desktop frame -->
          <div class="hidden sm:block w-full max-w-xs h-[500px] bg-[#63C57B] rounded-[3rem] p-2 shadow-2xl">
            <div class="w-full h-full bg-[#233375] rounded-[2.5rem] relative overflow-hidden">

            </div>
          </div>
        </div>
        <NewsCarousel/>
      </div>
    </div>
  </section>
</template>

<script setup>
import NewsCarousel from "./NewsCarousel.vue";
// import Press from "./Press.vue";
</script>