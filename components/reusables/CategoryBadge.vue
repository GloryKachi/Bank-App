<template>
  <div class="relative inline-block">

    <div class="w-[71px] h-[21px] rounded-[4px] overflow-hidden">
      <svg
          class="w-full h-full"
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="none"
          viewBox="0 0 100 100"
      >
        <defs>
          <pattern
              id="stripes"
              patternUnits="userSpaceOnUse"
              width="10"
              height="10"
              patternTransform="rotate(45)"
          >
            <rect width="5" height="10" fill="#0D2C65" />
            <rect x="5" width="5" height="10" fill="white" />
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#stripes)" />
      </svg>
    </div>


    <button
        class="absolute top-0 left-0 w-[70px] h-[20px] translate-x-[-1px] translate-y-[-1px] text-white text-[10px] rounded-[4px] font-medium leading-[14px] flex items-center justify-center"
        :style="{ backgroundColor: color }"
    >
      {{ label }}
    </button>
  </div>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    default: 'Category',
  },
  color: {
    type: String,
    default: '#2CD85F',
  },
});
</script>
