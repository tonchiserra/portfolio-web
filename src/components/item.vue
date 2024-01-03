<template>
  <div class="item">
    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="17" viewBox="0 0 20 17" fill="none">
      <path d="M6.61692 16.2979L0 9.63128L2.94249 6.66667L6.61692 10.3792L16.9083 0L19.8507 2.96461L6.61692 16.2979Z" fill="#1572B6"/>
    </svg>
    <p><slot></slot></p>
  </div>
</template>

<style scoped lang="scss">
.item {
  display: grid;
  grid-template-columns: 20px 1fr;
  align-items: center;
  gap: 40px;
}
</style>