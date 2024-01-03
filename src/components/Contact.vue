<template>
  <section id="Contact" class="contact-section">
    <div class="contact-container page-width">
      <h3>Let's make something<br>amazing <span>together</span>.</h3>

      <div class="email">
        <p class="message">Start by saying hi</p>
        <a href="mailto:serragonzalo1@gmail.com" class="underline">serragonzalo1@gmail.com</a>
      </div>

      <div class="social-networks">
        <a href="https://www.linkedin.com/in/serragonzalo/" target="_blank">LinkedIn</a>
        <a href="https://github.com/tonchiserra" target="_blank">GitHub</a>
        <a href="https://twitter.com/tonchiserra" target="_blank">Twitter / X</a>
        <a href="https://www.instagram.com/tonchiserra/" target="_blank">Instagram</a>
      </div>
    </div>

    <footer class="page-width footer-container">
      <p>Designed & developed by Gonzalo Serra.</p>
    </footer>
  </section>
</template>

<style scoped lang="scss">
.contact-section {
  padding-top: 90px;
  padding-bottom: 90px;
  min-height: 100dvh;
  display: flex;
  align-items: center;
  background-color: #fff;
  position: relative;

  .contact-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 80px;
    transform: translateY(-50px);

    h3 {
      text-align: center;

      span {
        color: var(--main-color);
      }
    }

    .email {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;

      .message {
        color: var(--text-color);
        font-size: 32px;
        font-weight: 400;
      }

    }
    
    .social-networks {
      display: flex;
      align-items: center;
      gap: 40px;

    }
  }

  .footer-container {
    border-top: 1px solid var(--gray-color-300);
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    margin: 0 auto;
    width: 100%;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>