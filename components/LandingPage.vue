<template>
  <header class="landing-page-container">
    <div class="logo-container">
      <div class="logo-container-1" />
      <div class="logo-container-2" />
      <div class="logo-container-3" />
      <div class="char-container">
        G
      </div>
    </div>
    <div class="logo-title">
      GEODEZJA
    </div>
    <div class="logo-subtitle">
      MARCIN TYLECKI
    </div>
  </header>
</template>

<script>
export default {
  name: 'LandingPage',
  components: {},
  data() {
    return {}
  }
}
</script>

<style scoped>
.landing-page-container {
  height: 100vh;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #7c2c35;
  font-family: Raleway, sans-serif;
}
.logo-container {
  width: 300px;
  height: 300px;
  position: relative;
  background: transparent;
}
.logo-container-1 {
  position: absolute;
  top: 60px;
  left: 60px;
  width: 180px;
  height: 180px;
  border: 2px solid #c5c5cc;
  background: transparent;
  animation: first-anim 0.5 both;
}
.logo-container-2 {
  position: absolute;
  top: 60px;
  left: 60px;
  width: 180px;
  height: 180px;
  border: 2px solid #c5c5cc;
  background: transparent;
  animation: second-anim 0.5s 0.5s both;
}
.logo-container-3 {
  position: absolute;
  top: 60px;
  left: 60px;
  width: 180px;
  height: 180px;
  border: 2px solid #c5c5cc;
  background: transparent;
  animation: third-anim 0.5s 0.5s both;
}
.char-container {
  position: absolute;
  top: 100px;
  left: 100px;
  width: 100px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 80px;
  font-family: Raleway, sans-serif;
  font-weight: 700;
  color: #c5c5cc;
  background: transparent;
  animation: first-anim 0.5s 1s both;
}
.logo-title {
  font-size: 50px;
  font-family: Raleway, sans-serif;
  font-weight: 500;
  letter-spacing: 5px;
  color: #c5c5cc;
  margin-bottom: 10px;
  animation: first-anim 0.5s 1s both;
}
.logo-subtitle {
  font-size: 20px;
  font-family: Raleway, sans-serif;
  font-weight: 500;
  letter-spacing: 3px;
  color: #c5c5cc;
  animation: first-anim 0.5s 1s both;
}
@keyframes first-anim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@keyframes second-anim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    transform: translate(15px, -15px);
  }
}
@keyframes third-anim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    transform: translate(-15px, 15px);
  }
}

@media (min-width: 400px) {
  .logo-title {
    font-size: 60px;
    letter-spacing: 10px;
  }
  .logo-subtitle {
    font-size: 30px;
  }
}
</style>
