<script setup>
import AboutMeSection from './components/AboutMeSection.vue'

import FooterSection from './components/FooterSection.vue'
import HeroSection from './components/HeroSection.vue'
import NavBar from './components/NavBar.vue'
import PathToFollow from './components/PathToFollow.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import SwiperSection from './components/SwiperSection.vue'
</script>

<template>
  <PathToFollow />
  <NavBar />
  <main class="absolute left-0 top-[100px] w-full">
    <HeroSection />
    <AboutMeSection />
    <div class="text-center">
      <button class="buttonPadding">CTA</button>
    </div>
    <ProjectsSection />
    <SwiperSection />
    <FooterSection />
  </main>
</template>

<style scoped></style>
