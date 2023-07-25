<script setup></script>

<template>
  <svg
    width="100"
    height="3703"
    viewBox="0 0 100 3703"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    class="absolute left-5 top-[-500px]"
  >
    <path
      d="M96.7248 2C48.9769 94.1844 -17.2752 426 43.1672 664.5C83.9532 773.967 91.2248 980.5 65.4579 1151.5C33.739 1362 31.5686 1597.07 68.2661 1722C85.7327 1781.46 88.8963 2036.28 29 2262.5C-27 2474 19.2226 2741.5 71.8613 2907C124.5 3072.5 72.357 3135 23.4285 3279C-25.5 3423 34.2266 3679.19 28 3701.5"
      stroke="#EC7566"
      stroke-width="7"
    />
  </svg>
</template>

<style scoped>
svg {
  stroke-dasharray: 100;
  stroke-dashoffset: 10000;
  animation: move 170s linear forwards infinite; /* Increased animation duration for a slower and smoother effect */
}

@keyframes move {
  0% {
    stroke-dashoffset: 10000;
  }
  50% {
    stroke-dashoffset: 100;
  }
  100% {
    stroke-dashoffset: 10000;
  }
}
</style>
