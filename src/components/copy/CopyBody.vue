<template>
  <p class="body"><slot /></p>
</template>
<style scoped>
.body {
  color: #87879d;
  font-size: 1rem;
  line-height: 1.625rem;
  margin-top: 1.5rem;
  margin-bottom: 2rem;
}

@media only screen and (min-width: 1440px) {
  .body {
    font-size: 1.125rem;
  }
}
</style>
