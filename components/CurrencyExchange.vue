<template>
  <div class="max-w-md mx-auto bg-white p-6 space-y-6">
    <!-- Send Amount -->
    <div class="space-y-2">
      <label class="text-sm text-[#8C8C8C]">You send</label>
      <div class="flex items-center justify-between bg-gray-50 rounded-lg p-4">
        <input
            v-model.number="sendAmount"
            type="number"
            class="bg-transparent border-none outline-none w-full text-[#0D2C65]"
            style="font-size: 24px; font-weight: 500; line-height: 32px"
            placeholder="1,000.00"
            @input="calculateConversion"
        />
        <div class="flex items-center space-x-2 bg-[#233375] w-[138px] h-[71px] text-white px-4 py-2 rounded-lg">
          <img src="https://flagcdn.com/w20/gb.png" alt="UK Flag" class="w-5 h-3" />
          <span class="font-medium">GBP</span>
        </div>
      </div>
    </div>

    <!-- Fee -->
    <div class="flex items-center space-x-2 text-gray-600">
      <div class="w-6 h-6 bg-black rounded-full flex items-center justify-center">
        <span class="text-white text-xs">-</span>
      </div>
      <span class="text-sm">{{ fee }} GBP Fee</span>
    </div>

    <!-- Receive Amount -->
    <div class="space-y-2">
      <label class="text-sm text-gray-500">Recipient Gets</label>
      <div class="flex items-center justify-between bg-gray-50 rounded-lg p-4">
        <span class="text-2xl text-[#0D2C65]" style="font-size: 24px; font-weight: 500; line-height: 32px;">
          {{ formatNumber(receiveAmount) }}
        </span>
        <div class="flex items-center justify-center space-x-2 bg-[#233375] w-[110px] h-[71px] text-white px-4 py-2 rounded-lg">
          <img src="https://flagcdn.com/w20/gh.png" alt="Ghana Flag" class="w-5 h-3" />
          <span class="font-medium">GHS</span>
        </div>
      </div>
    </div>

    <!-- Conversion Details -->
    <div class="flex items-center justify-between">
      <div>
        <p class="text-sm text-[#6F6F6F]">Amount we'll convert</p>
        <p class="text-lg text-[#0D2C65] py-1">{{ formatNumber(convertAmount) }}</p>
      </div>
      <div class="text-right">
        <div class="flex items-center">
          <!-- Clock icon as SVG instead of external file -->
          <svg class="mx-2 w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <circle cx="12" cy="12" r="10"></circle>
            <polyline points="12,6 12,12 16,14"></polyline>
          </svg>
          <p class="text-sm text-[#6F6F6F]">Guaranteed rate (1 hr)</p>
        </div>
        <p class="text-lg text-[#0D2C65] py-1">£1 / GHS{{ exchangeRate }}</p>
      </div>
    </div>

    <!-- Payment Summary -->
    <div class="flex items-center justify-between">
      <div>
        <p class="text-sm text-[#6F6F6F]">Total to Pay</p>
        <p class="text-lg text-[#0D2C65] py-1">{{ formatNumber(totalToPay) }} GBP</p>
      </div>
      <div class="text-right">
        <p class="text-sm text-[#6F6F6F]">Average duration</p>
        <p class="text-lg text-[#0D2C65] py-1">Instant</p>
      </div>
    </div>

    <!-- CTA Button -->
    <button
        class="w-full bg-[#233375] text-[#E6E6E6] py-4 rounded-[5px] font-semibold text-[16px] hover:bg-indigo-900 transition-colors"
        @click="handleGetStarted"
    >
      Get started for free
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const sendAmount = ref(1000)
const fee = ref(2.99)
const exchangeRate = ref(16.25) // Static fallback rate

const receiveAmount = computed(() => (sendAmount.value - fee.value) * exchangeRate.value)
const convertAmount = computed(() => sendAmount.value - fee.value)
const totalToPay = computed(() => sendAmount.value + fee.value)

function formatNumber(num: number): string {
  return new Intl.NumberFormat('en-GB', {
    minimumFractionDigits: 2,
    maximumFractionDigits: 2
  }).format(num)
}

function calculateConversion() {
  // In case you want to validate input later
}

function handleGetStarted() {
  console.log('Conversion started for', sendAmount.value)
}
</script>

<style scoped>
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
input[type="number"] {
  -moz-appearance: textfield;
}
</style>