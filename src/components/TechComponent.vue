<template>
  <div id="tech-main-container">
    <h2 id="tech-title">Tecnologías con las que he trabajado</h2>
    <DrawerComponent title="Frontend" :content="['Vue', 'Angular', 'Android (Java y Kotlin)', 'HTML+CSS+JS']" />
    <DrawerComponent title="Backend" :content="['Laravel', 'Symfony']" />
    <DrawerComponent title="Frameworks PHP" :content="['WordPress', 'Roundcube', 'Moodle']" />
  </div>
</template>
<script>
import DrawerComponent from './DrawerComponent.vue';

export default {
  components: {
    DrawerComponent
  }

}
</script>
<style scoped>
#tech-main-container {
  margin-top: 10px;
  padding-bottom: 10px;
}

#tech-title {
  text-align: center;
}
</style>
