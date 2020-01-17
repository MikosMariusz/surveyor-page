<template>
  <div v-if="loading" class="loader-back">
    <div class="loader" />
  </div>
</template>

<script>
export default {
  data: () => ({
    loading: false
  }),
  methods: {
    start() {
      this.loading = true
    },
    finish() {
      this.loading = false
    }
  }
}
</script>

<style>
.loader-back {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #7c2c35;
  z-index: 10;
}

.loader {
  border: 16px solid #f3f3f3; /* Light grey */
  border-top: 16px solid green; /* Blue */
  border-radius: 50%;
  width: 120px;
  height: 120px;
  animation: spin 0.8s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
