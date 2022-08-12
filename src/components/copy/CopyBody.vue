<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    props: {
      theme: {
        type: String,
        validator: (value: string) => ['dark', 'light'].includes(value),
        default: 'dark',
      },
    },
  })
</script>

<template>
  <p :class="['copy-body', theme]"><slot /></p>
</template>

<style scoped>
  .copy-body {
    color: #87879d;
    font-size: 1rem;
    font-weight: 500;
    line-height: 1.625rem;
    margin-top: 1.5rem;
    margin-bottom: 2rem;
    margin-left: 1.5rem;
    margin-right: 1.5rem;
  }

  .dark {
    color: #87879d;
  }

  .light {
    color: #fff;
    font-size: 1.125rem;
  }

  @media only screen and (min-width: 1440px) {
    .body {
      font-size: 1.125rem;
    }
  }
</style>
