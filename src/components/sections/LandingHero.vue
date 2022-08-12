<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    props: {
      title: String,
    },
  })
</script>

<template>
  <div class="hero">
    <slot />
  </div>
</template>

<style scoped>
  .hero {
    position: relative;
    overflow-x: hidden;
  }

  .hero:before {
    content: '';
    display: block;
    position: relative;
    background-image: url('../../assets/tablet/image-hero.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 110.4%;
    left: -50%;
    transform: translateX(50%);
    width: 100%;
    min-height: 153px;
    aspect-ratio: 414/153;
    margin-bottom: 3rem;
  }
</style>
