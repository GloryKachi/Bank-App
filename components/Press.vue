<template>
  <section
      class="relative flex items-center justify-start bg-gradient-to-br from-blue-50 to-indigo-100 px-6 min-h-screen"
  >
    <!-- Background Images -->
    <div class="absolute right-0 top-0 h-full w-full pointer-events-none">
      <img
          src="/images/press-bg-img.png"
          alt="bg shape 1"
          class="w-[400px] h-[650px] absolute right-0 top-0 opacity-10 mix-blend-multiply"
      />
      <img
          src="/images/press-bg-img2.png"
          alt="bg shape 2"
          class="w-[200px] h-[630px] absolute right-0 top-0 opacity-20 mix-blend-multiply "
      />
    </div>

    <!-- Content -->
    <div class="text-left mx-32 relative z-10">
      <div class="space-y-6">
        <!-- Main Heading -->
        <h2 class="leading-[77px] md:text-5xl font-[500] text-[#0D2C65]" style="font-size: 70px">
          Latest news and media<br />
          from around the world
        </h2>

        <!-- Description -->
        <p class="text-[#6E80A3] text-[24px] leading-[31px] max-w-md font-normal">
          Please write to us at
          <a
              href="mailto:media@bomba.co"
              class="text-[#6E80A3] underline"
          >
            media@bomba.co
          </a>
          if you have a media enquiry. We'll do our best to get back to you as soon as possible.
        </p>

        <!-- CTA Button -->
        <div class="pt-4">
          <button
              @click="handleGetPressKit"
              class="inline-flex items-center text-blue-600 hover:text-blue-800 font-medium transition-colors group"
          >
            Get press kit
            <svg
                class="mx-2 mt-1"
                width="24"
                height="24"
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

          <div class="mt-2 w-[133px] border-b border-[#2668EC] opacity-100"></div>
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
