<template>
  <div>
    <NavbarComponent id="navbar"></NavbarComponent>
    <main id="main">
      <AboutMeComponent />
      <TechComponent />
      <ContactComponent />

    </main>
    <footer>
      <FooterComponent></FooterComponent>
    </footer>

  </div>
</template>

<script>
import AboutMeComponent from './components/AboutMeComponent.vue';
import ContactComponent from './components/ContactComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import NavbarComponent from './components/NavbarComponent.vue';
import TechComponent from './components/TechComponent.vue';

export default {
  components: {
    NavbarComponent,
    AboutMeComponent,
    TechComponent,
    ContactComponent,
    FooterComponent,
  }
}
</script>

<style scoped></style>
