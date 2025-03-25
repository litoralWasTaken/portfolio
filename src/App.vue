<template>
  <div>
    <NavbarComponent id="navbar"></NavbarComponent>
    <main id="main">
      <AboutMeComponent></AboutMeComponent>

    </main>

  </div>
</template>

<script>
import AboutMeComponent from './components/AboutMeComponent.vue';
import NavbarComponent from './components/NavbarComponent.vue';

export default {
  components: {
    NavbarComponent,
    AboutMeComponent
  }
}
</script>

<style scoped></style>
