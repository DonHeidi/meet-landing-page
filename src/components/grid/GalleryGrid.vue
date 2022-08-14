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
      max-width: 1100px;
      margin-bottom: 3rem;
      margin-left: 2.5rem;
      margin-right: 2.5rem;
    }
  }

  @media only screen and (min-width: calc(1100px + 5rem)) {
    .grid {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>
