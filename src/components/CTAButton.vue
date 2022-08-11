<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    theme: {
      type: String,
      validator: (value: string) => ['primary', 'secondary'].includes(value),
      default: () => 'primary',
    },
  },
})
</script>

<template>
  <a :class="['cta', theme]" href="#"><slot /></a>
</template>

<style>
.cta {
  display: block;
  border-radius: 29px;
  padding-block: 1rem;
  align-items: center;
  text-decoration: none;
  margin-inline: auto;
  font-size: 1rem;
  text-decoration: none;
  color: white;
  font-weight: bold;
  width: fit-content;
}

.primary {
  background-color: aqua;
  padding-inline: 2.5rem;
}

.secondary {
  background-color: purple;
  padding-inline: 29px;
}

@media only screen and (min-width: 768px) {
  .cta {
    display: inline-block;
    margin-inline: 0.5rem;
  }
}
</style>
