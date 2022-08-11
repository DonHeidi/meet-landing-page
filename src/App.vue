<script lang="ts">
import { defineComponent } from 'vue'
import HeroSection from './components/LandingHero.vue'
import BrandLogo from './components/BrandLogo.vue'
import LandingSection from './components/LandingSection.vue'
import SectionCTA from './components/SectionCTA.vue'
import SectionGrid from './components/SectionGrid.vue'
import CTAButton from './components/cta/CTAButton.vue'
import CopyOverline from './components/copy/CopyOverline.vue'
import CopyHeading from './components/copy/CopyHeading.vue'
import CopySubHeading from './components/copy/CopySubHeading.vue'
import CopyBody from './components/copy/CopyBody.vue'

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
    CopyHeading,
    CopySubHeading,
    CopyBody,
  },
})
</script>

<template>
  <header>
    <BrandLogo />
    <HeroSection>
      <CopyHeading>Group Chat for Everyone</CopyHeading>
      <CopyBody
        >Meet makes it easy to connect with others face-to-face virtually and
        collaborate across any device.
      </CopyBody>
      <CTAButton theme="primary">Download <span>v1.3</span></CTAButton>
      <CTAButton theme="secondary">What is it?</CTAButton>
    </HeroSection>
  </header>
  <main>
    <LandingSection>
      <SectionGrid />
      <CopyOverline>Built for modern use</CopyOverline>
      <CopySubHeading>Smarter meetings, all in one place</CopySubHeading>
      <CopyBody>
        Send messages, share files, show your screen, and record your meetings —
        all in one workspace. Control who can join with invite-only team access,
        data encryption, and data export.
      </CopyBody>
    </LandingSection>
    <LandingSection>
      <SectionCTA>
        <CopySubHeading> Experience more together </CopySubHeading>
        <CopyBody
          >Stay connected with reliable HD meetings and unlimited one-on-one and
          group video sessions.
        </CopyBody>
        <CTAButton>Download <span>v1.3</span></CTAButton>
      </SectionCTA>
    </LandingSection>
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
}
</style>
