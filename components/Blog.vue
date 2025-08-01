<template>
  <div class="min-h-screen bg-white">
    <Press/>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6 sm:py-8 mt-8 sm:mt-16 lg:mt-32">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 sm:gap-6">
        <article
            v-for="article in articles"
            :key="article.id"
            class="bg-[#F8F9FE] rounded-lg overflow-hidden hover:shadow-lg transition-shadow duration-300 w-full"
        >

          <div class="p-3 sm:p-4 pb-2">
            <CategoryBadge :label="article.category" color="#2CD85F" />
          </div>


          <div class="px-3 sm:px-5 pb-3 sm:pb-4">
            <h2 class="font-semibold text-base sm:text-[17px] leading-tight sm:leading-[19px] text-[#0D2C65] mb-2 line-clamp-2">
              {{ article.title }}
            </h2>
            <div class="flex items-center text-sm text-gray-500 space-x-4">
              <span>{{ article.date }}</span>
            </div>
          </div>


          <div class="pt-3 sm:pt-4">
            <div class="w-full h-40 sm:h-48 rounded-sm overflow-hidden">
              <img
                  v-if="article.imageUrl"
                  :src="article.imageUrl"
                  :alt="article.imageAlt || article.title"
                  class="w-full h-full object-cover"
                  @error="handleImageError"
              />
              <div
                  v-else
                  class="w-full h-full flex items-center justify-center text-white font-bold text-base sm:text-lg p-2 text-center"
                  :class="getImageBackground(article.id)"
              >
                {{ article.imageText || article.title.substring(0, 20) + '...' }}
              </div>
            </div>
          </div>
        </article>
      </div>
    </main>
  </div>
</template>

<script setup lang="ts">
import CategoryBadge from "./reusables/CategoryBadge.vue";

interface Article {
  id: number;
  title: string;
  category: string;
  date: string;
  imageText?: string;
  imageUrl?: string;
  imageAlt?: string;
}

const articles: Article[] = [
  {
    id: 1,
    title: "Combining AI, fintech to solve African mobile inclusion",
    category: "FINTECH",
    date: "May 15, 2024",
    imageUrl: "/images/ai-img.svg",
    imageAlt: "AI and Fintech integration in Africa",
    imageText: "AI & FINTECH"
  },
  {
    id: 2,
    title: "Ghana to host the 14th Africa Fintech Summit on October 8th",
    category: "EVENT",
    date: "Sep 20, 2024",
    imageUrl: "/images/host-fintech.svg",
    imageAlt: "Africa Fintech Summit in Ghana",
    imageText: "AFRICA FINTECH SUMMIT"
  },
  {
    id: 3,
    title: "Midterm Report: Techstars Toronto's Second 2021 Class",
    category: "STARTUP",
    date: "Jul 12, 2024",
    imageUrl: "/images/tech-stars.svg",
    imageAlt: "Techstars Toronto accelerator program",
    imageText: "TECHSTARS TORONTO"
  },
  {
    id: 4,
    title: "Wise granted approval to join Zengin, Japan's domestic payment system",
    category: "FINTECH",
    date: "Jun 28, 2024",
    imageUrl: "/images/wise-img.svg",
    imageAlt: "Wise payment system in Japan",
    imageText: "WISE"
  },
  {
    id: 5,
    title: "African startups to participate at Techstars Toronto October 2021 cohort",
    category: "EVENT",
    date: "Oct 5, 2024",
    imageUrl: "/images/future-africa-img.svg",
    imageAlt: "African startups at Techstars",
    imageText: "TECHSTARS"
  },
  {
    id: 6,
    title: "More African startups get into Techstars Toronto",
    category: "STARTUP",
    date: "Aug 18, 2024",
    imageUrl: "/images/future-africa-img.svg",
    imageAlt: "Startup collaboration",
    imageText: "TECHSTARS"
  }
];

const getCategoryColor = (category: string): string => {
  const colors: Record<string, string> = {
    FINTECH: 'bg-green-500',
    EVENT: 'bg-blue-500',
    STARTUP: 'bg-purple-500',
    TECH: 'bg-orange-500'
  };
  return colors[category] || 'bg-gray-500';
};

const getImageBackground = (id: number): string => {
  const backgrounds = [
    'bg-gradient-to-br from-green-600 to-teal-700',
    'bg-gradient-to-br from-red-500 to-orange-600',
    'bg-gradient-to-br from-blue-600 to-indigo-700',
    'bg-gradient-to-br from-green-500 to-emerald-600',
    'bg-gradient-to-br from-purple-600 to-indigo-700',
    'bg-gradient-to-br from-purple-600 to-pink-700'
  ];
  return backgrounds[(id - 1) % backgrounds.length];
};

const handleImageError = (event: Event) => {
  const img = event.target as HTMLImageElement;
  const fallbackDiv = img.parentElement;
  if (fallbackDiv) {
    fallbackDiv.innerHTML = `
      <div class="w-full h-full flex items-center justify-center text-white font-bold text-lg bg-gradient-to-br from-gray-600 to-gray-700">
        Image not found
      </div>
    `;
  }
};
</script>

<style scoped>
.line-clamp-2 {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
</style>