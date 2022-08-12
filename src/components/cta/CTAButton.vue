<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    theme: {
      type: String,
      validator: (value: string) => ['primary', 'secondary'].includes(value),
      default: () => 'primary',
    },
    padding: {
      type: String,
      validator: (value: string) => ['sm', 'lg'].includes(value),
      default: () => 'lg',
    },
  },
})
</script>

<template>
  <a :class="['cta', theme, `p-${padding}`]" href="#"><slot /></a>
</template>

<style>
.cta {
  display: block;
  color: #fff;
  font-weight: 900;
  font-size: 1rem;
  line-height: 1.625rem;
  text-decoration: none;

  padding-top: 1rem;
  padding-bottom: 1rem;
  margin: 1rem auto;

  border-radius: 29px;

  align-items: center;

  width: fit-content;
}

.primary {
  background-color: #4d96a9;
  padding-inline: 2.5rem;
}

.primary:hover {
  background-color: #71c0d4;
}

.secondary {
  background-color: #855fb1;
}

.secondary:hover {
  background-color: #d9b8ff;
}

.p-sm {
  padding-inline: 29px;
}

.p-lg {
  padding-inline: 40px;
}

@media only screen and (min-width: 768px) {
  .cta {
    display: inline-block;
    margin-inline: 0.5rem;
  }
}
</style>
