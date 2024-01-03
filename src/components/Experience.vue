<script setup lang="ts">
import ExperienceSnippet from './ExperienceSnippet.vue'
import ProjectCard from './ProjectCard.vue'
import { Splide } from '@splidejs/vue-splide'
import { IProject } from '../interfaces/projectInterface.js'

const projects: IProject[] = [
  {
    title: "Valery Accesorios",
    subtitle: "Contribution - Innovate Group",
    description: "Layout and development of Shopify e-commerce components based on a mockup that the design team provided me. The highlight component developed by me is the infinite promo bar that appears in the header and others places of the store.",
    technologies: ["shopify", "javascript", "vue", "sass", "css", "html"],
    repo: "",
    demo: "https://valeryaccesorios.com.ar/",
    image: ""
  },
  {
    title: "Mac Center",
    subtitle: "Contribution - Innovate Group",
    description: "I developed differents features and fix some issues in the Mac Center store. This is a Premium Partner Reseller of Apple, is a big store with multiples shops at Colombia, Perú, Panamá and República Dominicana.",
    technologies: ["shopify", "javascript", "vue", "sass", "css", "html"],
    repo: "https://mac-center.com/",
    demo: "",
    image: ""
  }
]

let splideProjectsOptions = {
  type: 'loop',
  width: '100vw',
  perPage: window.innerWidth > 680 ? 1.5 : 1.2,
  perMove: 1,
  focus: 'center',
  gap: window.innerWidth > 680 ? '100px' : '40px',
  updateOnMove: true,
  pagination: false,
  autoplay: true,
  interval: 7000,
  pauseOnHover: true,
  drag: window.innerWidth > 680 ? false : true
}
</script>

<template>
  <section id="Experience" class="experience-section">
    <div class="experience-container page-width">
      <h3>Professional experience</h3>
      <div class="professional-experiences">
        <ExperienceSnippet />
      </div>
    </div>

    <div class="title page-width">
      <h3>Projects & Contributions</h3>
      <a href="https://github.com/tonchiserra" class="underline">View all my repositories</a>
    </div>
    <div class="side-projects">
      <Splide :options="splideProjectsOptions" class="slide-projects" aria-label="Projects & contributions">
        <ProjectCard v-for="(project, index) in projects" :key="index" :project="project" />
      </Splide>
    </div>
  </section>
</template>

<style scoped lang="scss">
.experience-section {
  padding-bottom: 40px;

  .experience-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding-top: 90px;
    padding-bottom: 40px;
    gap: 40px;
  }

  .title {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    width: 100%;

    a {
      margin-bottom: 5px;
    }
  }
}
</style>