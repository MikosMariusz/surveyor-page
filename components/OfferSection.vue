<template>
  <section :id="sectionid">
    Oferta
  </section>
</template>

<script>
export default {
  name: 'OfferSection',
  props: {
    sectionid: {
      type: String,
      required: true
    }
  },
  scrollToTop: true
}
</script>

<style scoped></style>
