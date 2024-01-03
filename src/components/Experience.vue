<script setup lang="ts">
import ExperienceSnippet from './ExperienceSnippet.vue'
import ProjectCard from './ProjectCard.vue'
import { Splide, SplideTrack } from '@splidejs/vue-splide'
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

const perPage = (): number => {
  if(window.innerWidth > 1200) return 2 
  if(window.innerWidth > 680) return 1.5
  if(window.innerWidth < 680) return 1.2

  return 1
}

let splideProjectsOptions = {
  type: 'loop',
  width: '100vw',
  perPage: perPage(),
  perMove: 1,
  focus: 'center',
  gap: window.innerWidth > 680 ? '100px' : '40px',
  updateOnMove: true,
  pagination: false,
  autoplay: true,
  interval: 8000,
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
      <Splide :has-track="false" :options="splideProjectsOptions" class="slide-projects" aria-label="Projects & contributions">
        <SplideTrack>
          <ProjectCard v-for="(project, index) in projects" :key="index" :project="project" />
        </SplideTrack>

        <div class="splide__arrows">
          <button class="splide__arrow splide__arrow--prev">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M16.17 13L12.59 16.59L14 18L20 12L14 6L12.59 7.41L16.17 11H4V13H16.17Z" fill="#1572B6"/>
            </svg>
          </button>
          <button class="splide__arrow splide__arrow--next">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M16.17 13L12.59 16.59L14 18L20 12L14 6L12.59 7.41L16.17 11H4V13H16.17Z" fill="#1572B6"/>
            </svg>
          </button>
        </div>
      </Splide>
    </div>
  </section>
</template>

<style scoped lang="scss">
.experience-section {
  padding-bottom: 90px;

  .experience-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding-top: 90px;
    padding-bottom: 90px;
    gap: 60px;
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

  .splide__arrow {
    background-color: #fff;
    height: 48px;
    width: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 1;
    filter: drop-shadow(0px 4px 16px rgba(34, 34, 34, 0.10));
    bottom: 26px;
    top: unset;
    transform: unset;
    transition: all 300ms ease;

    &:hover {
      transform: scale(1.2);
    }

    &--prev {
      left: calc(50% - 68px);      
    }

    &--next {
      right: calc(50% - 68px);
    }

    svg {
      width: 24px;
      height: 24px;
    }
  }
}
</style>