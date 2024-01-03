<template>
  <section id="Home" class="home-section">
    <div class="page-width home-container">
      <h1>Hey! I'm <span>Gonzalo</span></h1>
      <h2>Web Developer & Shopify Expert Dev</h2>

      <a href="https://www.linkedin.com/in/serragonzalo/" target="_blank" class="button">Let's talk</a>

      <img src="../assets/profile-pic.svg" alt="Profile pic" />
    </div>
  </section>
</template>

<style scoped lang="scss">
.home-section {
  background-color: var(--second-color);

  .home-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    min-height: 100dvh;
    position: relative;
    text-align: center;

    .button {
      display: none;
      margin-top: 60px;

      @media screen and (max-width: 680px) {
        display: flex;
      }
    }

    h1 {
      margin-top: 110px;

      @media screen and (max-width: 680px) {
        font-size: 5rem;

        span {
          font-size: 7rem;
        }
      }

      span {
        color: var(--main-color);
      }
    }

    h2 {
      margin-top: 20px;

      @media screen and (max-width: 680px) {
        font-size: 2.8rem;
        margin-top: 30px;
      }
    }

    img {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      margin: 0 auto;

      @media screen and (max-width: 680px) {
        width: calc(100dvw - 40px);
      }
    }
  }
}
</style>