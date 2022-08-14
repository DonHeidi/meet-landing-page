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
    height: 40.8vw;
    width: 100%;
    margin-bottom: 3rem;
    overflow-x: hidden;
  }

  @media only screen and (min-width: 768px) {
    .hero:before {
      background-size: 106.4%;
      margin-bottom: 4.5rem;
    }
  }

  @media only screen and (min-width: 1440px) {
    .hero:before {
      position: absolute;
      background-image: url('../../assets/desktop/image-hero-left.png');
      background-size: contain;
      background-position: -2rem;
      transform: none;
      left: 0rem;
      top: -50px;
      height: 303px;
      width: 33%;
    }

    .hero:after {
      overflow-x: hidden;
      content: '';
      position: absolute;
      background-image: url('../../assets/desktop/image-hero-right.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: calc(100% + 2rem);
      transform: none;
      right: 0rem;
      bottom: 9px;
      height: 303px;
      width: 33%;
    }
  }
</style>
