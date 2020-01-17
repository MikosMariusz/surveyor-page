<template>
  <div class="sidenav-container">
    <div v-if="show" @click="toggle" class="sidenav-backdrop" />
    <transition name="slide-side">
      <div v-if="show" class="sidenav">
        <ul @click="toggle" class="nav-list">
          <li class="nav-item">
            <a href="#about">O nas</a>
          </li>
          <li class="nav-item">
            <a href="#offer">Oferta</a>
          </li>
          <li class="nav-item">
            <a href="#contact">Kontakt</a>
          </li>
        </ul>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'TheSidenav',
  props: {
    show: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    toggle() {
      this.$emit('close')
    }
  }
}
</script>

<style scoped>
.sidenav-container {
  height: 100%;
  width: 100%;
}

.sidenav-backdrop {
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 1000;
  position: fixed;
  top: 0;
  left: 0;
}

.sidenav {
  height: 100%;
  width: 250px;
  background-color: #202020;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  z-index: 10000;
  position: fixed;
  top: 0;
  left: 0;
  box-sizing: border-box;
  border-right: 1px solid #c5c5cc;
  padding: 30px;
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
}

.slide-side-enter-active,
.slide-side-leave-active {
  transition: all 0.3s ease-in-out;
}
.slide-side-enter,
.slide-side-leave-to {
  transform: translateX(-100%);
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  text-align: right;
  margin: 20px 0;
}

.nav-item a {
  text-decoration: none;
  color: #c5c5cc;
  font-family: Raleway, sans-serif;
  font-size: 25px;
  font-weight: 300;
  line-height: 2.5;
}

.nav-item a:hover,
.nav-item a:active {
  color: #7c2c35;
}

@media (max-height: 650px) {
  .nav-item a {
    font-size: 20px;
    line-height: 1.8;
  }
}

@media (max-height: 400px) {
  .nav-item a {
    font-size: 15px;
    line-height: 1.5;
  }
}
</style>
