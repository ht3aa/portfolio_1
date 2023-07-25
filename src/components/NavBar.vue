<script setup></script>

<template>
  <nav
    class="w-full bg-[#161B22] sm:bg-transparent absolute left-0 top-0 sm:flex items-center px-6 py-5 z-50"
  >
    <img class="w-[60px] mx-auto sm:mx-0 h-[60px] rounded-full" src="/imgs/logo.png" alt="logo" />
    <ul
      class="flex mt-3 sm:mt-0 sm:ml-7 w-full sm:w-[400px] justify-between items-center text-white"
    >
      <li><a href="#hero">Home</a></li>
      <li><a href="#aboutMe">About me</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#customers">Customers</a></li>
    </ul>
  </nav>
</template>

<style scoped>
ul li:hover {
  cursor: pointer;
}
</style>
