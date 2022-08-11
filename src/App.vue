<script lang="ts">
import { defineComponent } from 'vue'
import HeroSection from './components/LandingHero.vue'
import BrandLogo from './components/BrandLogo.vue'
import LandingSection from './components/LandingSection.vue'
import SectionGrid from './components/SectionGrid.vue'
import SectionCTA from './components/SectionCTA.vue'

export default defineComponent({
  name: 'App',
  components: {
    HeroSection,
    BrandLogo,
    LandingSection,
    SectionGrid,
    SectionCTA,
  },
})
</script>

<template>
  <header>
    <BrandLogo />
    <HeroSection />
  </header>
  <main>
    <LandingSection><SectionGrid /></LandingSection>
    <LandingSection><SectionCTA /></LandingSection>
  </main>
</template>

<style>
*,
*:after,
*:before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
