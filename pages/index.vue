<template>
  <div>
    <LandingPage />
    <AboutSection sectionid="about" />
    <OfferSection sectionid="offer" />
    <ContactSection sectionid="contact" />
    <EUFundingSection sectionid="donation" />
  </div>
</template>

<script>
import LandingPage from '@/components/LandingPage'
import OfferSection from '@/components/OfferSection'
import AboutSection from '@/components/AboutSection'
import ContactSection from '@/components/ContactSection'
import EUFundingSection from '@/components/EUFundingSection'

export default {
  layout: 'section',
  scrollToTop: true,
  components: {
    LandingPage,
    AboutSection,
    OfferSection,
    ContactSection,
    EUFundingSection
  }
}
</script>
