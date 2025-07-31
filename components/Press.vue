<template>
  <section class="relative flex items-center justify-start bg-gradient-to-br from-blue-50 to-indigo-100 px-4 sm:px-6 lg:px-8 min-h-screen pt-8 sm:pt-0">
    <!-- Background Images -->
    <div class="absolute right-0 top-0 h-full w-full pointer-events-none overflow-hidden">
      <img
          src="/images/press-bg-img.png"
          alt="bg shape 1"
          class="w-[200px] sm:w-[300px] lg:w-[400px] h-[400px] sm:h-[500px] lg:h-[650px] absolute right-0 top-0 opacity-10 mix-blend-multiply"
      />
      <img
          src="/images/press-bg-img2.png"
          alt="bg shape 2"
          class="w-[100px] sm:w-[150px] lg:w-[200px] h-[400px] sm:h-[500px] lg:h-[630px] absolute right-0 top-0 opacity-20 mix-blend-multiply"
      />
    </div>

    <!-- Content -->
    <div class="text-left max-w-7xl mx-auto w-full relative z-10">
      <div class="space-y-4 sm:space-y-6 max-w-4xl">
        <!-- Main Heading -->
        <h2 class="text-[70px] md:text-[70px] font-[500] text-[#0D2C65] leading-[77px]">
          Latest news and media<br />
          from around the world
        </h2>

        <!-- Description -->
        <p class="text-[#6E80A3] text-lg sm:text-xl lg:text-[24px] leading-relaxed sm:leading-[1.3] lg:leading-[31px] max-w-2xl font-normal">
          Please write to us at
          <a
              href="mailto:media@bomba.co"
              class="text-[#6E80A3] underline hover:text-blue-600 transition-colors"
          >
            media@bomba.co
          </a>
          if you have a media enquiry. We'll do our best to get back to you as soon as possible.
        </p>

        <!-- CTA Button -->
        <div class="pt-2 sm:pt-4">
          <button
              @click="handleGetPressKit"
              class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition-colors group text-base sm:text-lg"
          >
            Get press kit
            <svg
                class="ml-2 mt-0.5 group-hover:translate-x-1 transition-transform duration-200"
                width="20"
                height="20"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
            >
              <path
                  d="M16.2419 13.4141L16.2419 7.75727M16.2419 7.75727L10.585 7.75727M16.2419 7.75727L7.7566 16.2425"
                  stroke="#2668EC"
                  stroke-width="1.5"
                  stroke-linecap="square"
                  stroke-linejoin="round"
              />
            </svg>
          </button>
          <div class="mt-2 w-[100px] sm:w-[133px] border-b border-[#2668EC] opacity-100"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const handleGetPressKit = () => {
  console.log('Getting press kit...')
}
</script>