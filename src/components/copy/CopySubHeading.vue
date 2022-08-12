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
  <h2 :class="['sub-heading', theme]"><slot /></h2>
</template>
<style scoped>
  .dark {
    color: #28283d;
  }

  .light {
    color: #fff;
  }

  .sub-heading {
    font-size: 2rem;
    line-height: 2.25rem;
    font-weight: 900;
    margin: 1.5rem;
  }

  @media only screen and (min-width: 768px) {
    .sub-heading {
      font-size: 2.5rem;
      line-height: 2.75rem;
      margin-top: 1rem;
      margin-left: auto;
      margin-right: auto;
      max-width: 445px;
    }

    .light {
      margin-bottom: 2rem;
    }
  }
</style>
