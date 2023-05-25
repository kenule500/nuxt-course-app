<template>
  <div class="p-12 bg-gray-100 w-full h-full min-h-screen flex flex-col items-center">
    <div class="prose mb-12">
      <h1>
        <span class="font-medium text-[25px]">
          Course:
          <span class="font-bold">Mastering Nust</span>
        </span>
      </h1>
    </div>

    <div class="flex flex-row justify-center flex-grow">
      <div class="prose mr-4 p-8 bg-white rounded-md min-w[40ch] flex flex-col space-y-5 max-w-[30ch]">
        <h2 class="font-bold">Chapters</h2>
        <div class="space-y-1 mb-4 flex flex-col" v-for="chapter in chapters" :key="chapter.slug">
          <p class="text-[14px] font-bold">{{ chapter.title }}</p>
          <NuxtLink
            v-for="(lesson, index) in chapter.lessons"
            :key="lesson.slug"
            class="flex space-x-1 no-underline prose-sm font-normal py-1"
            :to="lesson.path"
            :class="{ 'text-blue-500': lesson.path === $route.fullPath }"
          >
            <span class="text-gray-500">{{ index + 1 }}.</span>
            <span>{{ lesson.title }}</span>
          </NuxtLink>
        </div>
      </div>
      <div class="prose p-12 bg-white rounded-md w-[65ch]">
        <NuxtPage />
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
const { chapters } = useCourse();
</script>
<!-- 
<style scoped>
.router-link-active {
  @apply text-blue-500;
}
</style> -->
