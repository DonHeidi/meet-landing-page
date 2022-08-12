<script lang="ts">
  import { defineComponent } from 'vue'

  export default defineComponent({
    props: {
      theme: {
        type: String,
        default: 'light',
        validator: (value: string) => ['light', 'dark'].includes(value),
      },
      footer: {
        type: Boolean,
        default: false,
      },
    },
  })
</script>

<template>
  <section :class="[footer ? 'footer' : 'section', theme]">
    <div class="numeration"></div>
    <slot />
  </section>
</template>

<style scoped>
  .section {
    margin-top: 8.25rem;
  }
  .footer {
    margin-top: 9.25rem;
    padding-bottom: 4rem;
  }

  .dark {
    position: relative;
  }

  .dark:before {
    content: '';
    background: url('../../assets/mobile/image-footer.jpg');
    position: absolute;
    background-size: cover;
    background-repeat: no-repeat;
    margin-top: 28px;
    height: calc(100% - 28px);
    width: 100%;
    left: 0;
    top: 0;
    z-index: -2;
  }

  .dark:after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    height: calc(100% - 28px);
    width: 100%;
    background-color: rgba(77, 150, 169, 0.9);
    margin-top: 28px;
    background-position-y: 50px;
    z-index: -1;
  }

  .numeration {
    position: relative;
    height: 3.5rem;
    aspect-ratio: 1/1;
    border-radius: 50%;
    border-color: rgba(135, 135, 157, 0.25);
    border-width: 1px;
    border-style: solid;
    background-color: #fff;
    text-align: center;
    vertical-align: middle;
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

  .numeration:after {
    position: absolute;
    color: #87879d;
    font-weight: 900;
    font-size: 1rem;
    line-height: 1.625rem;
    left: 50%;
    transform: translate(-50%, 50%);
  }

  .section .numeration:after {
    content: '01';
  }

  .footer .numeration:after {
    content: '02';
  }
</style>
