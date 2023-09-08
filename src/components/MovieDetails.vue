<template>
  <div v-if="movie" class="z-40 text-white pt-20 w-[50%]">
    <h1 class="text-[55px] font-semibold font-serif">{{ movie.name }}</h1>
    <div class="flex items-center text-lg pt-4">
      <span>{{ movie.year }}</span>
      <div class="relative">
        <span class="absolute left-[2px] -top-[12px] text-[40px]">.</span>
        <span class="pl-4">{{ movie.genre.one }}</span>
      </div>
      <div class="relative">
        <span class="absolute left-[2px] -top-[12px] text-[40px]">.</span>
        <span class="pl-4">{{ movie.genre.two }}</span>
      </div>
      <div class="relative">
        <span class="absolute left-[2px] -top-[12px] text-[40px]">.</span>
        <span class="pl-4">{{ movie.genre.three }}</span>
      </div>
    </div>
    <p class="text-2xl pt-6">{{ movie.description }}</p>
  </div>
</template>

<script setup>
defineProps({
  movie: Object,
});
</script>
