<template>
  <button @click="toggle" class="drawer-toggle">
    <span class="box">
      <span class="inner" />
    </span>
  </button>
</template>

<script>
export default {
  methods: {
    toggle() {
      this.$emit('toggle')
    }
  }
}
</script>

<style scoped>
.drawer-toggle {
  display: inline-block;
  padding-left: 15px;
  background-color: transparent;
  border: 0;
  margin: 0;
  cursor: pointer;
  z-index: 1001;
}

@media (min-width: 800px) {
  .drawer-toggle {
    display: none;
  }
}

.box {
  width: 40px;
  height: 24px;
  display: inline-block;
  position: relative;
}

.inner {
  width: 100%;
  height: 3px;
  background-color: #c5c5cc;
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  transition: background-color 0.1s 0.2s ease-in-out;
}

.inner::before {
  content: '';
  width: 100%;
  height: 3px;
  top: -10px;
  left: 0;
  background-color: #c5c5cc;
  position: absolute;
}

.inner::after {
  content: '';
  width: 100%;
  height: 3px;
  top: 10px;
  left: 0;
  background-color: #c5c5cc;
  position: absolute;
}
</style>
