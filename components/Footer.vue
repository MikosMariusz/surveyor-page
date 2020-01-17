/* eslint-disable vue/html-self-closing */
<template>
  <footer class="primary--text footer-container">
    <div class="ending">
      <p>
        © {{ new Date().getFullYear() }}
        <a ref="https://www.mariuszmikos.pl/">
          Mariusz Mikoś. All rights reserved.
        </a>
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>

<style scoped>
.footer-container {
  position: relative;
  left: 0;
  bottom: 0;
  width: 100%;
  padding: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #202020;
  color: #c5c5cc;
  box-shadow: 0 -5px 28px rgba(0, 0, 0, 0.3), 0 -3px 10px rgba(0, 0, 0, 0.22);
  font-family: Raleway, sans-serif;
  font-weight: 300;
}

a {
  text-decoration: none;
}
</style>
