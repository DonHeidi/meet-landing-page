<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    },
  },
})
</script>

<template>
  <img class="grid-img" :src="src" :alt="alt ? alt : ''" />
</template>

<style scopded>
.grid-img {
  width: 100%;
  border-radius: 0.5rem;
}
</style>
