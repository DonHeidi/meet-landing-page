<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    number: Number,
  },
})
</script>

<template>
  <section class="section">
    <div class="numeration"></div>
    <slot />
  </section>
</template>

<style scoped>
.section {
  margin-top: 9.25rem;
}

.section:first-of-type .numeration:after {
  content: '01';
}

.section:nth-of-type(2) .numeration:after {
  content: '02';
}

.numeration:after {
  color: #87879d;
  font-weight: 900;
  font-size: 1rem;
  line-height: 1.625rem;
}

.numeration {
  position: relative;
  height: 4.5rem;
  aspect-ratio: 1/1;
  border-radius: 50%;
  border-color: rgba(135, 135, 157, 0.25);
  border-width: 1px;
  border-style: solid;
  text-align: center;
  line-height: 4.5rem;
  margin-left: auto;
  margin-right: auto;
  margin-top: 84px;
  margin-bottom: 4rem;
}

.numeration::before {
  content: '';
  width: 1px;
  height: 84px;
  background-color: rgba(135, 135, 157, 0.25);
  position: absolute;
  top: -84px;
  left: 50%;
  transform: translateX(-50%);
}
</style>
