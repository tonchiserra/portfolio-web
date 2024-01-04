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
  background-color: $second-color;

  .home-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    min-height: 100dvh;
    position: relative;
    text-align: center;

    .button {
      display: none;
      margin-top: 60px;

      @include mobile-only {
        display: flex;
      }
    }

    h1 {
      margin-top: 110px;

      @include mobile-only {
        font-size: 5rem;

        span {
          font-size: 7rem;
        }
      }

      span {
        color: $main-color;
      }
    }

    h2 {
      margin-top: 20px;

      @include mobile-only {
        font-size: 2.8rem;
        margin-top: 30px;
      }
    }

    img {
      margin-top: 100px;
      
      @include mobile-only {
        width: calc(100dvw - 40px);
      }
    }
  }
}
</style>