<template>
  <div>
    <LandingPage />
    <AboutSection sectionid="about" />
    <OfferSection sectionid="offer" />
    <ContactSection sectionid="contact" />
  </div>
</template>

<script>
import LandingPage from '@/components/LandingPage'
import OfferSection from '@/components/OfferSection'
import AboutSection from '@/components/AboutSection'
import ContactSection from '@/components/ContactSection'

export default {
  layout: 'section',
  scrollToTop: true,
  components: {
    LandingPage,
    AboutSection,
    OfferSection,
    ContactSection
  }
}
</script>
