<template>
  <div id="contact-main-container">
    <h2>¡Ponte en contacto!</h2>

    <div class="my-btn" @click="goTo('linkedin')">
      <FontAwesomeIcon icon="fa-brands fa-linkedin" /> LinkedIn
    </div>
    <div class="my-btn" @click="goTo('gh')">
      <FontAwesomeIcon icon="fa-brands fa-github" /> GitHub
    </div>
    <div class="contact-mail">
      O mándame un correo a rglopez300@gmail.com
    </div>
  </div>
</template>
<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  components: {
    FontAwesomeIcon
  },

  methods: {
    goTo(site) {
      let url = '';
      switch (site) {
        case 'linkedin':
          url = 'https://linkedin.com/in/rglopezandroid'
          break;

        case 'gh':
          url = 'https://github.com/litoralWasTaken'
          break;
      }

      window.open(url, '_blank')
    }
  },
}
</script>
<style scoped>
#contact-main-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 10px;
  text-align: center;
}

.my-btn {
  width: 10em;
  text-align: center;
}

.contact-mail {
  margin-top: 10px;
}
</style>
