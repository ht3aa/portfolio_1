<script setup></script>

<template>
  <section id="aboutMe" class="mx-auto w-[90%] md:w-[70%] my-[120px] bg-[#161B22] boxBorder">
    <div class="flex relative items-center windowActionBorder justify-center px-5 pt-3 pb-4">
      <div class="hidden md:flex justify-between items-center absolute left-7 top-6 w-[70px]">
        <div class="w-[15px] h-[15px] rounded-full bg-[#05FF00]"></div>
        <div class="w-[15px] h-[15px] rounded-full bg-[#FFF500]"></div>
        <div class="w-[15px] h-[15px] rounded-full bg-[#FF0000]"></div>
      </div>
      <div class="flexCenterBetween w-[350px] text-[#7A7A7B] bg-[#0C1015] px-5 py-2 rounded-full">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M16.5 10.5V6.75a4.5 4.5 0 10-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 002.25-2.25v-6.75a2.25 2.25 0 00-2.25-2.25H6.75a2.25 2.25 0 00-2.25 2.25v6.75a2.25 2.25 0 002.25 2.25z"
          />
        </svg>
        <p>About me</p>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M16.023 9.348h4.992v-.001M2.985 19.644v-4.992m0 0h4.992m-4.993 0l3.181 3.183a8.25 8.25 0 0013.803-3.7M4.031 9.865a8.25 8.25 0 0113.803-3.7l3.181 3.182m0-4.991v4.99"
          />
        </svg>
      </div>
      <div></div>
    </div>
    <div class="flex flex-col md:flex-row items-center md:items-stretch py-5 justify-around">
      <div class="w-[90%] text-center md:text-start md:w-[45%] px-5 py-9 bg-[#0C1015]">
        <h2 class="text-4xl mb-4 text-white">About me</h2>
        <p>
          orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
          been the industry's standard dummy text ever since the 1500s, when an unknown printer took
          a galley of type and scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap into electronic typesetting, remaining essentially
          unchanged.
        </p>
      </div>
      <div class="w-[90%] md:w-[45%] px-5 py-9 bg-[#0C1015]">
        <img class="w-[300px] mx-auto" src="/imgs/me.jpg" alt="me image" />
      </div>
    </div>
  </section>
</template>
<style scoped>
.windowActionBorder {
  border-bottom: 1px solid #7a7a7b;
}
</style>
