<template>
  <section :id="sectionid">
    <div class="wraper">
      <img src="../static/dofinansowanie.jpg">
    </div>
  </section>
</template>

<script>
export default {
  name: 'EUFundingSection',
  props: {
    sectionid: {
      type: String,
      required: true
    }
  },
  scrollToTop: true
}
</script>

<style scoped>
.wraper {
  border: 1px solid #7c2c35;
  box-shadow: 0 5px 28px rgba(0, 0, 0, 0.3), 0 3px 10px rgba(0, 0, 0, 0.22);
  width: 90%;
  height: auto;
}

img {
  width: 100%;
}

@media (min-width: 1200px) {
  .wraper {
    width: 70%;
  }
}
</style>