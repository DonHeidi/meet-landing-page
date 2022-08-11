<script lang="ts">
import { defineComponent } from 'vue'
import HeroSection from './components/LandingHero.vue'
import BrandLogo from './components/BrandLogo.vue'
import LandingSection from './components/LandingSection.vue'
import SectionGrid from './components/SectionGrid.vue'
import SectionCTA from './components/SectionCTA.vue'
import CTAButton from './components/CTAButton.vue'
import CopyOverline from './components/CopyOverline.vue'

export default defineComponent({
  name: 'App',
  components: {
    HeroSection,
    BrandLogo,
    LandingSection,
    SectionGrid,
    SectionCTA,
    CTAButton,
    CopyOverline,
  },
})
</script>

<template>
  <header>
    <BrandLogo />
    <HeroSection>
      <h1>Group Chat for Everyone</h1>
      <p>
        Meet makes it easy to connect with others face-to-face virtually and
        collaborate across any device.
      </p>

      <CTAButton theme="primary">Download <span>v1.3</span></CTAButton>
      <CTAButton theme="secondary">What is it?</CTAButton>
    </HeroSection>
  </header>
  <main>
    <LandingSection>
      <SectionGrid />
      <CopyOverline>Built for modern use</CopyOverline>
      <h2>Smarter meetings, all in one place</h2>
      <p>
        Send messages, share files, show your screen, and record your meetings —
        all in one workspace. Control who can join with invite-only team access,
        data encryption, and data export.
      </p>
    </LandingSection>
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
