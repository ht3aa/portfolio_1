<script setup>
import FlyingTools from '../components/FlyingTools.vue'
</script>

<template>
  <footer id="footer" class="bg-[#161B22] py-5">
    <div class="mx-auto w-[300px] text-center">
      <img
        class="w-[60px] h-[60px] object-cover mx-auto rounded-full mb-3"
        src="/imgs/logo.png"
        alt="logo image"
      />
      <p>
        Made by<br />
        <a class="text-[#EC7566] underline" href="https://www.hasaweb.tech">www.hasanweb.tech</a>
      </p>
    </div>
    <FlyingTools />
  </footer>
</template>
