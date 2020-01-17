<template>
  <div>
    <Navbar
      :show="displaySidenav"
      @sidenavToggle="displaySidenav = !displaySidenav"
    />
    <SideNav :show="displaySidenav" @close="displaySidenav = false" />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Footer from '@/components/Footer'
import SideNav from '@/components/SideNav'

export default {
  components: {
    Navbar,
    SideNav,
    Footer
  },
  scrollToTop: true,
  data() {
    return {
      displaySidenav: false
    }
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  overflow-y: scroll;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

::-webkit-scrollbar {
  width: 0px;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  background-color: #c5c5cc;
}
</style>
