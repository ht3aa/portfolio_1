<script setup>
defineProps({
  title: String,
  description: String,
  ctaLink: String,
  imgLink: String
})
</script>

<template>
  <div class="boxBorder text-center flex flex-col justify-between pb-4">
    <img class="boxBorderBottom" :src="imgLink" alt="project image" />

    <div class="p-4 items-stretch">
      <h4 class="text-2xl text-white">{{ title }}</h4>
      <p class="my-5">{{ description }}</p>
    </div>
    <div>
      <a :href="ctaLink">
        <button class="px-4 py-1 w-[60%] bg-[#161B22] text-white">Read More</button>
      </a>
    </div>
  </div>
</template>

<style scoped></style>
