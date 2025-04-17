<template>
  <div id="about-me-bg">
    <img id="about-me-my-photo" src="/photo.jpg" alt="Mi foto">
    <div id="about-me-text">
      ¡Hola! Mi nombre es <span id="about-me-my-name">Rodrigo García López</span>, soy un desarrollador de la
      Comunidad de Madrid. Aunque
      estoy graduado en desarrollo web full-stack, también he adquirido experiencia en diversos entornos, especialmente
      en
      el desarrollo de aplicaciones Android.
    </div>

    <div class="my-btn" @click="downloadCV()">
      Descarga mi CV
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    downloadCV() {

      // Define the PDF file path (relative to public/)
      const fileUrl = "https://github.com/litoralWasTaken/portfolio/blob/master/public/cv.pdf"; // Adjust the file name if needed

      // Create a temporary anchor element
      const a = document.createElement("a");
      a.href = fileUrl;
      a.download = "rodrigo-garcia-cv.pdf"; // The file name for download
      document.body.appendChild(a);
      a.click();

      // Cleanup
      document.body.removeChild(a);

    }
  },

}
</script>
<style scoped>
#about-me-bg {
  padding-top: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
}



#about-me-my-photo {
  padding: 10px;
  width: auto;
  height: 200px;
}

#about-me-text {
  padding: 10px;
}

#about-me-my-name {
  color: var(--secondary-text);
}
</style>
