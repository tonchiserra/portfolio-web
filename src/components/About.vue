<script setup lang="ts">
import Item from "./Item.vue";
</script>

<template>
  <section id="AboutMe" class="about-section">
    <div class="page-width about-container">
      <div class="left">
        <h3>Who am I?</h3>
        <p>
          My name is Gonzalo but you can call me Tonchi. From Totoras, Santa Fe, Argentina, I'm 22 years old and passionate about the IT world.
          <br><br>
          In 2019 I started to study Systems Engineering at National Technological University but in 2023 I realized that university is not for me, I prefeer self-taught learning. So, this is how I focus on learning and improving my skills as a web developer.
        </p>
      </div>
      
      <div class="right">
        <h3>What can i do?</h3>
        <div class="items">
          <Item>Develop awesome sections and features that will take your store to the next level.</Item>
          <Item>Give support to Shopify stores using Liquid.</Item>
          <Item>Develop full-stack web applications with HTML, CSS/Sass, Javascript, Vue.js and NodeJS.</Item>
          <Item>Design systems applying MVC pattern and Vertical Slice architecture.</Item>
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
    background-color: var(--second-color);
    padding-top: 90px;
    padding-bottom: 90px;
    min-height: 100dvh;
    display: flex;
    align-items: center;

    .about-container {
      display: grid;
      grid-template-columns: 1fr 50%;
      gap: 120px;

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
        gap: 40px;
        margin-top: 60px;

        h3 {
          color: var(--main-color);
          padding: 0;
          font-variant-numeric: lining-nums proportional-nums;
        }

        p {
          font-weight: 700;
        }
      }
    }
  }

</style>