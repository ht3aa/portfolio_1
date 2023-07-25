<script setup>
import { tools } from '../assets/data'
</script>

<template>
  <div
    class="absolute z-[-1] p-2 w-max boxBorder rounded-full"
    :style="{
      animationDuration: `${Math.floor(Math.random() * (50 - 10 + 1)) + 10}s`,
      right: `${Math.floor(Math.random() * 50)}%`,
      bottom: `-${Math.floor(Math.random() * 10)}%`
    }"
    v-for="tool in tools"
    :key="tool.id"
  >
    <img class="w-[20px] rounded-full" :src="tool.img" alt="tool image" />
  </div>
</template>

<style scoped>
div {
  animation: fly linear infinite;
}
@keyframes fly {
  from {
    bottom: 0px;
  }
  to {
    bottom: 10000px;
  }
}
</style>
