<template>
  <div id="footer-main-container">
    <FontAwesomeIcon class="copy-icon" icon="fa-regular fa-copyright" />
    <div>
      Rodrigo García López, 2025
    </div>



  </div>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  components: {
    FontAwesomeIcon
  }
}
</script>
<style scoped>
#footer-main-container {
  background-color: gray;
  color: var(--text);
  height: 150px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;

  font-size: small;
}

.copy-icon {
  margin-right: 5px;
}
</style>
