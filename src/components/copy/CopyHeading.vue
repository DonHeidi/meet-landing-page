<template>
  <h1 class="heading"><slot /></h1>
</template>
<style scoped>
  .heading {
    color: #28283d;
    font-size: 2.5rem;
    font-weight: 900;
    line-height: 2.75rem;
    margin: 1.5rem;
    white-space: pre-line;
  }

  @media only screen and (min-width: 1440px) {
    .heading {
      font-size: 4rem;
      line-height: 4rem;
    }
  }

  @media only screen and (min-width: 768px) {
    .heading {
      font-size: 3rem;
      line-height: 3rem;
    }
  }
</style>
