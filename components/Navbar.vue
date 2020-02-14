<template>
  <div id="nav-container">
    <SideNavToggle @toggle="$emit('sidenavToggle')" />
    <nav>
      <ul>
        <li><a href="#about">O nas</a></li>
        <li><a href="#offer">Oferta</a></li>
        <li><a href="#contact">Kontakt</a></li>
        <li><a href="#donation">Dofinansowanie</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
import SideNavToggle from '@/components/SideNavToggle'

export default {
  components: {
    SideNavToggle
  },
  props: {
    show: {
      type: Boolean,
      default: false
    }
  },
  mounted() {
    // eslint-disable-next-line space-before-function-paren
    this.$nextTick(function() {
      // eslint-disable-next-line space-before-function-paren
      window.addEventListener('scroll', function() {
        const navbar = document.getElementById('nav-container')
        const navclasses = navbar.classList
        if (document.documentElement.scrollTop >= 50) {
          if (navclasses.contains('shrink') === false) {
            navclasses.toggle('shrink')
          }
        } else if (navclasses.contains('shrink') === true) {
          navclasses.toggle('shrink')
        }
      })
    })
  }
}
</script>

<style scoped>
#nav-container {
  position: fixed;
  top: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 80px;
  background-color: #7c2c35;
  border-bottom: 1px solid #c5c5cc;
  border: none;
  box-shadow: none;
  z-index: 100;
  font-family: Raleway, sans-serif;
  font-weight: 300;
  transition: all 0.5s ease;
}

#nav-container.shrink {
  height: 60px;
  background-color: #202020;
  border-bottom: 1px solid #c5c5cc;
  box-shadow: 0 5px 28px rgba(0, 0, 0, 0.3), 0 3px 10px rgba(0, 0, 0, 0.22);
}

ul {
  display: none;
  list-style: none;
  width: 100%;
  justify-content: center;
}

li {
  margin: 0 1rem;
  padding: 1rem;
}

a {
  text-decoration: none;
  text-transform: uppercase;
  color: #c5c5cc;
  font-size: 20px;
}

a:hover,
a:active {
  color: #202020;
}

#nav-container.shrink a:hover,
#nav-container.shrink a:active {
  color: #7c2c35;
}

@media (min-width: 800px) {
  #nav-container {
    justify-content: center;
  }

  ul {
    display: flex;
  }
}
</style>
