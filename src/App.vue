<script lang="ts">
  import { defineComponent } from 'vue'
  import HeroSection from './components/sections/LandingHero.vue'
  import BrandLogo from './components/BrandLogo.vue'
  import LandingSection from './components/sections/LandingSection.vue'
  import CTAButton from './components/cta/CTAButton.vue'
  import CopyOverline from './components/copy/CopyOverline.vue'
  import CopyHeading from './components/copy/CopyHeading.vue'
  import CopySubHeading from './components/copy/CopySubHeading.vue'
  import CopyBody from './components/copy/CopyBody.vue'
  import GalleryGrid from './components/grid/GalleryGrid.vue'
  import GalleryImage from './components/grid/GalleryImage.vue'
  import CTASubLabel from './components/cta/CTASubLabel.vue'

  export default defineComponent({
    name: 'App',
    components: {
      HeroSection,
      BrandLogo,
      LandingSection,
      CTAButton,
      CopyOverline,
      CopyHeading,
      CopySubHeading,
      CopyBody,
      GalleryGrid,
      GalleryImage,
      CTASubLabel,
    },
    data: () => {
      return {
        hero: {
          headline: 'Group Chat\nfor Everyone',
          copyHero:
            'Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.',
        },
        main: {
          womanInVideoCall: require('@/assets/desktop/image-woman-in-videocall.jpg'),
          womenVideochatting: require('@/assets/desktop/image-women-videochatting.jpg'),
          menInMeeting: require('@/assets/desktop/image-men-in-meeting.jpg'),
          manTexting: require('@/assets/desktop/image-man-texting.jpg'),
          title: 'Smarter meetings, all in one place',
          overline: 'Built for modern use',
          copy: 'Send messages, share files, show your screen, and record your meetings — all in one workspace. Control who can join with invite-only team access, data encryption, and data export.',
        },
        footer: {
          title: 'Experience more together',
          copy: 'Stay connected with reliable HD meetings and unlimited one-on-one and group video sessions.',
        },
        download: {
          label: 'Download',
          subLabel: 'v1.3',
        },
        about: {
          label: 'What is it?',
        },
      }
    },
  })
</script>

<template>
  <header>
    <BrandLogo />
    <HeroSection>
      <CopyHeading>{{ hero.headline }}</CopyHeading>
      <CopyBody>{{ hero.copyHero }}</CopyBody>
      <CTAButton>
        {{ download.label }}
        <CTASubLabel>
          {{ download.subLabel }}
        </CTASubLabel>
      </CTAButton>
      <CTAButton theme="secondary" padding="sm">{{ about.label }}</CTAButton>
    </HeroSection>
  </header>
  <main>
    <LandingSection>
      <GalleryGrid>
        <GalleryImage :src="main.womanInVideoCall" alt="" />
        <GalleryImage :src="main.womenVideochatting" alt="" />
        <GalleryImage :src="main.menInMeeting" alt="" />
        <GalleryImage :src="main.manTexting" alt="" />
      </GalleryGrid>
      <CopyOverline>{{ main.overline }}</CopyOverline>
      <CopySubHeading>{{ main.title }}</CopySubHeading>
      <CopyBody>{{ main.copy.replace('-', '&#8209;') }}</CopyBody>
    </LandingSection>
  </main>
  <footer>
    <LandingSection theme="dark" footer>
      <CopySubHeading theme="light">{{ footer.title }}</CopySubHeading>
      <CopyBody theme="light">{{ footer.copy }}</CopyBody>
      <CTAButton theme="secondary">
        {{ download.label }}
        <CTASubLabel>
          {{ download.subLabel }}
        </CTASubLabel>
      </CTAButton>
    </LandingSection>
  </footer>
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Red+Hat+Display:wght@500;900&display=swap');
  *,
  *:after,
  *:before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #app {
    font-family: 'Red Hat Display', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
  }
</style>
