<script setup lang="ts">
import Item from "./Item.vue";
</script>

<template>
  <div class="experience-snippet">
    <div class="company">
      <h4>Innovate Group</h4>
      <p>July 2022 - Present</p>
    </div>

    <div class="timeline">
      <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" viewBox="0 0 45 45" fill="none">
        <circle cx="22.5" cy="22.5" r="22" stroke="#C4C4C4" stroke-dasharray="10 10"/>
        <circle cx="22.5" cy="22.5" r="11.5" fill="#B9DCFF"/>
      </svg>
      <div class="line"></div>
      <div class="bg-gradient"></div>
    </div>

    <div class="description">
      <div class="company">
        <h4>Innovate Group</h4>
        <p>July 2022 - Present</p>
      </div>

      <h4>Web Dev & Shopify Dev</h4>
      <Item>I was working in the support area solving technical problems of different clients with Shopify Stores.</Item>

      <Item>I created different components using top web technologies like Liquid, Vue.js, TypeScript and Sass.</Item>

      <Item>I learned how to create and deploy backend developments like automations or AWS Lambdas using Node.js and Express.</Item>

      <Item>I worked with more than 80 Shopify Stores including Zumba, Mac-Center, Nestle, Cole Haan and Plant The Future.</Item>
    </div>
  </div>
</template>

<style scoped lang="scss">
.experience-snippet {
  width: 100%;
  display: grid;
  grid-template-columns: 300px 50px 1fr;
  gap: 40px;

  .company {
    display: flex;
    flex-direction: column;
    padding-top: 10px;

    p {
      font-size: 1.4rem;
      font-weight: 600;
    }
  }

  .timeline {
    display: grid;
    grid-template-rows: 45px 1fr;
    position: relative;

    svg {
      transform: rotate(23deg);
    }

    .line {
      height: 100%;
      margin: 0 auto;
      width: 1px;
      transform: translateX(-2px);
      position: relative;
      overflow: hidden;

      &::before {
        content: "";
        position: absolute;
        left: -3px;
        bottom: 0;
        top: 0;
        border-right: 6px dashed $gray-color-300;
      }
    }

    .bg-gradient {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      margin: 0 auto;
      width: 45px;
      height: 170px;
      background: linear-gradient(0deg, #FFF 3.65%, rgba(255, 255, 255, 0.00) 100%);
    }
  }

  .description {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-bottom: 50px;
    padding-top: 10px;

    .company {
      display: none;
    }
  }
}

@include mobile-only {
  .experience-snippet {
    grid-template-columns: 50px 1fr;
    gap: 20px;

    .company {
      display: none;
    }

    .description {
      .company {
        display: flex;
        padding: 0;
      }

      .item {
        gap: 20px;
      }
    }
  }
}
</style>