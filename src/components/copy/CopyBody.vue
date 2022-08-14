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

  @media only screen and (min-width: 457px) {
    header .copy-body {
      width: 457px;
      margin-left: auto;
      margin-right: auto;
    }
  }

  @media only screen and (min-width: 768px) {
    .copy-body {
      width: 573px;
      margin-left: auto;
      margin-right: auto;
    }

    footer .copy-body,
    .footer .copy-body {
      margin-bottom: 2.5rem;
    }
    header .copy-body {
      width: 457px;
      margin-left: auto;
      margin-right: auto;
    }
  }

  @media only screen and (min-width: 1440px) {
    .copy-body {
      font-size: 1.125rem;
    }

    header .copy-body {
      margin-top: 2.125rem;
    }

    footer .copy-body {
      margin-bottom: 0px;
      margin-left: 125px;
      margin-right: 92px;
    }
  }
</style>
