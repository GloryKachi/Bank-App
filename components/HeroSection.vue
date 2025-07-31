<template>
  <section class="bg-light-gray py-16 lg:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Vertical layout with centered content -->
      <div class="flex flex-col items-center justify-center gap-12 text-center">

        <!-- Phone Frame -->
        <div class="flex justify-center">
          <div class="w-64 max-w-full h-[500px] bg-[#63C57B] rounded-[3rem] p-2 shadow-2xl">
            <div class="w-full h-full bg-[#233375] rounded-[2.5rem] relative overflow-hidden">
            </div>
          </div>
        </div>
        <!-- Text Content -->
        <NewsCarousel/>


      </div>
    </div>
  </section>

<!--  <Press/>-->
</template>

<script setup>
import NewsCarousel from "./NewsCarousel.vue";
// import Press from "./Press.vue";
</script>
