<script setup lang="ts">
import Item from "./Item.vue";
</script>

<template>
  <section id="AboutMe" class="about-section">
    <div class="page-width about-container">
      <div class="left">
        <h3>Who am I?</h3>
        <p>
          My name is Gonzalo but you can call me Tonchi. From Totoras, Santa Fe, Argentina, I'm <strong>22 years</strong> old and passionate about the IT world.
          <br><br>
          In 2019 I started to study Systems Engineering at National Technological University but in 2023 I realized that university is not for me, I prefeer <strong>self-taught learning</strong>. So, this is how I focus on learning and improving my skills as a <strong>Web Developer</strong>.
          <br><br>
          Two years ago, in 2022, I discovered <strong>Shopify</strong> and its potential. I was caught by the satisfaction I got from seeing how companies grew and increased their sales thanks to the changes and features that my team and I developed. Since then, I work as Shopify Developer and <strong>I'm always looking for new challenges</strong>.
        </p>
      </div>
      
      <div class="right">
        <h3>What can i do?</h3>
        <div class="items">
          <Item>Develop awesome sections and features that will <strong>take your store to the next level.</strong></Item>
          <Item>Give support to Shopify stores using <strong>Liquid</strong>.</Item>
          <Item>Develop full-stack web applications with <strong>HTML</strong>, <strong>CSS/Sass</strong>, <strong>TypeScript</strong>, <strong>Vue.js</strong> and <strong>NodeJS</strong>.</Item>
          <Item>Design systems applying <strong>MVC pattern</strong> and <strong>Vertical Slice architecture</strong>.</Item>
        </div>

        <div class="numbers">
          <div class="number">
            <h3>100+</h3>
            <p>Stores worked</p>
          </div>
          <div class="number">
            <h3>2</h3>
            <p>Years experience</p>
          </div>
          <div class="number">
            <h3>2500+</h3>
            <p>Contributions per year</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .about-section{
    background-color: $second-color;
    padding-top: 90px;
    padding-bottom: 90px;
    min-height: 100dvh;
    display: flex;
    align-items: center;

    .about-container {
      display: grid;
      grid-template-columns: 1fr 50%;
      gap: 120px;

      @include mobile-only {
        grid-template-columns: 1fr;
      }

      h3 {
        padding-bottom: 60px;
      }

      .items {
        display: flex;
        flex-direction: column;
        gap: 20px;
      }

      .numbers {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        flex-wrap: wrap;
        gap: 40px;
        margin-top: 60px;

        h3 {
          color: $main-color;
          padding: 0;
        }

        p {
          font-weight: 700;
        }
      }
    }
  }

</style>