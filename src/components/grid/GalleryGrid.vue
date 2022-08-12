<template>
  <div class="grid">
    <slot />
  </div>
</template>

<style scoped>
  .grid {
    display: grid;
    place-items: center;
    grid-template-columns: 1fr 1fr;
    column-gap: 25px;
    row-gap: 24px;
    margin-left: 1.5rem;
    margin-right: 1.5rem;
    margin-bottom: 4rem;
  }

  @media only screen and (min-width: 768px) {
    .grid {
      grid-template-columns: 1fr 1fr 1fr 1fr;
      margin-bottom: 3rem;
    }
  }
</style>
