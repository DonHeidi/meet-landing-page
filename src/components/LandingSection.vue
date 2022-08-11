<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    number: Number,
  },
})
</script>

<template>
  <section>
    <div class="numeration"></div>
    <slot />
  </section>
</template>

<style scoped>
section:first-of-type .numeration:after {
  content: '01';
}

section:nth-of-type(2) .numeration:after {
  content: '02';
}

.numeration {
  position: relative;
  height: 4.5rem;
  aspect-ratio: 1/1;
  border-radius: 50%;
  border-color: black;
  border-width: 2px;
  border-style: solid;
  text-align: center;
  line-height: 4.5rem;
  margin-left: auto;
  margin-right: auto;
  margin-top: 84px;
}

.numeration::before {
  content: '';
  width: 2px;
  height: 84px;
  background-color: black;
  position: absolute;
  top: -84px;
  left: 50%;
  transform: translateX(-50%);
}
</style>
