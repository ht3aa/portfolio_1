<script setup>
import Card from './Card.vue'
import { projectsData } from '../assets/data'
import { ref, onMounted } from 'vue'

const INCREASE_BY = 6
const projectsToShow = ref(0)
const projects = ref([])
const showMoreBtn = ref(true)

const showMore = () => {
  projectsToShow.value += INCREASE_BY
  projects.value = projectsData.slice(0, projectsToShow.value)

  console.log(projectsToShow.value, projectsData.length)
  if (projectsToShow.value > projectsData.length - 1) {
    showMoreBtn.value = false
    return
  }
}

const showLess = () => {
  projectsToShow.value -= INCREASE_BY
  projects.value = projectsData.slice(0, projectsToShow.value)

  if (projectsToShow.value <= INCREASE_BY) {
    showMoreBtn.value = true
    return
  }
}

onMounted(() => {
  if (showMoreBtn.value) {
    showMore()
  } else {
    showLess()
  }
})
</script>

<template>
  <section id="projects" class="mx-auto w-[90%] md:w-[70%] my-[120px]">
    <div class="customGrid">
      <Card
        v-for="(project, index) in projects"
        :key="index"
        :title="project.title"
        :description="project.description"
        :ctaLink="project.ctaLink"
        :imgLink="project.img"
      />
    </div>
    <div v-if="showMoreBtn" class="text-center my-[70px]">
      <button @click="showMore" class="buttonPadding">Show More</button>
    </div>
    <div v-else class="text-center my-[70px]">
      <button @click="showLess" class="buttonPadding">Show Less</button>
    </div>
  </section>
</template>

<style scoped>
.customGrid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}
</style>
