<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { customersOpinion } from '../assets/data'
// Import Swiper styles
import 'swiper/css'

const swiperRef = ref(null)
const currentSlideSet = ref(0)
let INCREASE_BY = 0
const slideBerView = ref(0)
if (window.screen.width < 768) {
  INCREASE_BY = 1
  slideBerView.value = 1
} else {
  INCREASE_BY = 3
  slideBerView.value = 3
}

const next = () => {
  if (currentSlideSet.value >= customersOpinion.length - 1) return
  currentSlideSet.value += INCREASE_BY

  swiperRef.value.slideToLoop(currentSlideSet.value, 1000)
}

const prev = () => {
  if (currentSlideSet.value <= 0) return
  currentSlideSet.value -= INCREASE_BY
  swiperRef.value.slideToLoop(currentSlideSet.value, 1000)
}

const onSwiper = (swiper) => {
  console.log(swiper)
  swiperRef.value = swiper
  swiperRef.value
}
const onSlideChange = () => {
  console.log('slide change')
}
</script>

<template>
  <section id="customers" class="mx-auto w-[70%] my-[120px]">
    <div class="boxBorder text-white p-5">
      <swiper
        :slides-per-view="slideBerView"
        :space-between="55"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide v-for="customer in customersOpinion" :key="customer.id">
          <div class="text-center">
            <img
              class="w-[60px] mx-auto h-[60px] object-cover rounded-full"
              :src="customer.img"
              alt="hero image"
            />
            <h4 class="text-2xl">{{ customer.name }}</h4>
            <p>{{ customer.text }}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
    <div class="mx-auto w-[150px] flex justify-between my-9">
      <button class="" @click="prev">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-8 h-8 text-[#7A7A7B] boxBorder bg-[#0C1015]"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M18.75 19.5l-7.5-7.5 7.5-7.5m-6 15L5.25 12l7.5-7.5"
          />
        </svg>
      </button>
      <button @click="next">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-8 h-8 text-[#7A7A7B] boxBorder bg-[#0C1015]"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M11.25 4.5l7.5 7.5-7.5 7.5m-6-15l7.5 7.5-7.5 7.5"
          />
        </svg>
      </button>
    </div>
  </section>
</template>

<style scoped>
/* Your existing styles */

.navigationButtons {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}

.navigationButtons button {
  margin: 0 10px;
  padding: 8px 16px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
