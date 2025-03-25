<template>
  <navbar>
    <div class="navbar-component-bg navbar-component-closed">
      <div class="navbar-title-container">
        <div class="navbar-component-title">
          Portfolio
        </div>
        <FontAwesomeIcon @click="toggleNavbar" class="navbar-hamburger" icon="fa-solid fa-bars" />
      </div>
    </div>
    <ul v-if="isMenuOpen" class="navbar-component-bg">
      <a href="#">
        <li>Sobre mí</li>
      </a>
      <a href="#">
        <li>Proyectos</li>
      </a>
      <a href="#">
        <li>Tecnologías</li>
      </a>
      <a href="#">
        <li>Contacto</li>
      </a>
    </ul>
  </navbar>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
export default {
  components: {
    FontAwesomeIcon
  },
  data() {
    return {
      isMenuOpen: false,
    }
  },

  methods: {
    toggleNavbar() {
      this.isMenuOpen = !this.isMenuOpen
    }
  },
}
</script>
<style scoped>
ul {
  list-style-type: none;
  padding-left: 10px;
}

a {
  text-decoration: none;
}

.navbar-component-bg {
  background-color: blueviolet;
  color: white;
}

.navbar-component-closed {
  height: 50px;
  line-height: 50px;
}

.navbar-component-title {
  margin-left: 10px;
}

.navbar-title-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.navbar-hamburger {
  width: 25px;
  height: 25px;
  margin-top: 10px;
  margin-right: 5px;

}
</style>
