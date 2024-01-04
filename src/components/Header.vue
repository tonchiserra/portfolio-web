<script lang="ts">
document.addEventListener("scroll", () => {
  const header = document.querySelector<HTMLElement>("header")
  if(!header) return

  const scrollPosition = window.scrollY
  scrollPosition > 65 ? header.classList.add("scroll") : header.classList.remove("scroll")
});
</script>

<template>
  <header>
    <div class="page-width header-container">
      <a href="/" class="logotype">GS</a>

      <dialog id="menu" class="menu">
        <form method="dialog">
          <button class="menu-btn transparent">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M17.59 5L12 10.59L6.41 5L5 6.41L10.59 12L5 17.59L6.41 19L12 13.41L17.59 19L19 17.59L13.41 12L19 6.41L17.59 5Z" fill="#2E3A59"/>
            </svg>
          </button>
        </form>
        <nav class="main-menu">
          <ul>
            <li><a class="alternative" href="#Home" onclick="menu.close()">HOME</a></li>
            <li><a class="alternative" href="#Experience" onclick="menu.close()">EXPERIENCE</a></li>
            <li><a class="alternative" href="#AboutMe" onclick="menu.close()">ABOUT ME</a></li>
            <li><a class="alternative" href="#Contact" onclick="menu.close()">CONTACT</a></li>
          </ul>
        </nav>
      </dialog>

      <a href="https://www.linkedin.com/in/serragonzalo/" target="_blank" class="button">Let's talk</a>

      <button class="menu-btn transparent" onclick="menu.showModal()">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
          <path d="M21 18H3V16H21V18ZM21 13H3V11H21V13ZM21 8H3V6H21V8Z" fill="#2E3A59"/>
        </svg>
      </button>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  background-color: $second-color;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  z-index: 3;

  &.scroll {
    border-bottom: 1px solid $gray-color-200;
  }

  .menu-btn {
    display: none;
    transition: all 300ms ease;

    &:hover {
      transform: scale(1.2);
    }

    @include mobile-only {
      display: block;
    }
  }

  .menu {
    display: block;
    position: unset;
    background: unset;
    border: unset;
  
    @include mobile-only {
      border: unset;
      width: 70dvw;
      height: 100%;
      right: 0;
      left: unset;
      transition: all 300ms ease;
      animation: modal 300ms cubic-bezier(0.785, 0.135, 0.15, 0.86) both alternate;
      max-height: unset;
      transform: translateX(75vw);
      position: fixed;
      background-color: #fff;
      display: none;

      &[open] {
        display: block;
      }

      nav ul {
        flex-direction: column;
      }

      form {
        padding: 2rem 2rem 1rem;
      }

      &::backdrop {
        background: #000A;
      }

    }
  }

  @keyframes modal {
    to {
      transform: translateX(0);
      opacity: 1;
    }
  }

  .header-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    height: 7rem;
  }

  .logotype {
    font-size: 4rem;
    color: $main-color;
    font-weight: 700;

    &:hover {
      transform: scale(1.2);
    }
  }

  .button {
    display: flex;

    @include mobile-only {
      display: none;
    }
  }

  .main-menu {
    ul {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 40px;
    }

    li {
      list-style: none;
    }
  }
}
</style>