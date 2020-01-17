<template>
  <section :id="sectionid">
    O nas
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
  props: {
    sectionid: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped></style>
