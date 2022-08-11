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
    <h1>Group Chat for Everyone</h1>
    <p>
      Meet makes it easy to connect with others face-to-face virtually and
      collaborate across any device.
    </p>
  </div>
  <a class="cta download" href="#">Download <span>v1.3</span></a>
  <a class="cta about" href="#">What is it?</a>
  <div class="grid"></div>
</template>

<style scoped>
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

@media only screen and (min-width: 768px) {
  .cta {
    display: inline-block;
    margin-inline: 0.5rem;
  }
}

.download {
  background-color: aqua;
  padding-inline: 2.5rem;
}

.about {
  background-color: purple;
  padding-inline: 29px;
}

.hero {
  position: relative;
  overflow-x: hidden;
}

.hero:before {
  content: '';
  display: block;
  position: relative;
  background-image: url('../assets/tablet/image-hero.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: 110.4%;
  left: -50%;
  transform: translateX(50%);
  width: 100%;
  min-height: 153px;
  aspect-ratio: 414/153;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  overflow-x: hidden;
}
</style>
