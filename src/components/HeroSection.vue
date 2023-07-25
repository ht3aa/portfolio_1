<script setup></script>

<template>
  <section
    id="hero"
    class="mx-auto mt-[130px] w-[90%] text-center md:text-start md:w-[60%] text-white"
  >
    <div
      class="information boxBorder flex items-center pr-[55px] pl-3 py-2 rounded-full mx-auto md:mx-0 w-max"
    >
      <img class="rounded-full mr-2 w-[35px] h-[35px]" src="/imgs/logo.png" alt="logo" />
      <h6 class="text-sm">Hasan Tahseen</h6>
    </div>
    <h1 class="text-5xl md:text-6xl font-bold mt-3">Main Header</h1>
    <p class="text-sm my-5 w-[80%] mx-auto md:mx-0 md:w-[70%]">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
      been the industry's standard dummy text ever since the
    </p>
    <button class="buttonPadding">CTA</button>
  </section>
</template>

<style scoped>
.information {
  background: linear-gradient(232deg, rgba(12, 13, 21, 0.44) 0%, #0c1015 100%);
}
</style>
