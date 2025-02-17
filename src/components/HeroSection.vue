<template>
  <section class="hero">
    <div class="intro">
      <h1>Hola, soy <span>Seán Alberdi</span> <span class="emoji">👋</span></h1>
      <br>
      <p class="title">Full Stack Developer.</p>
    </div>
    <div class="buttons">
      <button @click="$emit('scrollToContact')">Contáctame</button>
      <button @click="downloadCV">📥 Descargar CV</button>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    // Método para descargar el CV
    downloadCV() {
      const link = document.createElement("a");
      link.href = "/cv.pdf";
      link.download = "cv.pdf";
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }
  }
};
</script>

<style scoped lang="scss">
.hero {
  position: relative;
  text-align: center;
  padding: 370px 20px;
  color: white;
  z-index: 1; /* Aseguramos que el contenido de la hero esté encima de cualquier fondo */
}

.intro {
  display: inline-block;
  text-align: center; /* Centramos el texto en todo el contenedor */
  margin-bottom: 20px;
}

.intro h1 {
  font-size: 2.5rem;
  margin: 0;
}

.intro h1 span {
  color: #A389DA !important;
}

.emoji {
  color: inherit; /* Asegura que el emoji no tenga color aplicado */
}

.title {
  font-size: 1.25rem;
  margin-top: 10px;
  text-align: center; /* Asegura que el texto de Full Stack Developer esté centrado */
}

.buttons {
  margin-top: 20px;
}

.hero button {
  margin: 10px;
  z-index: 2; /* Asegura que el botón esté por encima de cualquier fondo */
}
</style>
