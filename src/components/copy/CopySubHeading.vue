<template>
  <h2 class="sub-heading"><slot /></h2>
</template>
<style scoped>
.sub-heading {
  color: #28283d;
  font-size: 2rem;
  line-height: 2.25rem;
  font-weight: 900;
}

@media only screen and (min-width: 768px) {
  .sub-heading {
    font-size: 2.5rem;
    line-height: 2.75rem;
  }
}
</style>
