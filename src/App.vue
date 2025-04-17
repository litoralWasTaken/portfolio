<template>
  <div>
    <NavbarComponent id="navbar"></NavbarComponent>
    <main id="main">
      <AboutMeComponent />
      <TechComponent />
    </main>
    <footer>
      <FooterComponent></FooterComponent>
    </footer>

  </div>
</template>

<script>
import AboutMeComponent from './components/AboutMeComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import NavbarComponent from './components/NavbarComponent.vue';
import TechComponent from './components/TechComponent.vue';

export default {
  components: {
    NavbarComponent,
    AboutMeComponent,
    TechComponent,
    FooterComponent
  }
}
</script>

<style scoped></style>
