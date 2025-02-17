<template>
  <div id="app">
    <NavBar />
    <HeroSection @scrollToContact="scrollToContact" />
    <AboutSection />
    <ProjectsSection />
    <ContactSection ref="contactSection" />
    <FooterSection />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import HeroSection from "@/components/HeroSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import ProjectsSection from "@/components/ProjectsSection.vue";
import ContactSection from "@/components/ContactSection.vue";
import FooterSection from "@/components/FooterSection.vue";

export default {
  components: {
    NavBar,
    HeroSection,
    AboutSection,
    ProjectsSection,
    ContactSection,
    FooterSection,
  },
  methods: {
    scrollToContact() {
      this.$refs.contactSection.$el.scrollIntoView({ behavior: 'smooth' });
    }
  },
};
</script>

<style>
body {
  background-color: #202124; /* Fondo original */
  color: white;
  margin: 0;
  font-family: 'Arial', sans-serif;
  position: relative;
  overflow-x: hidden; /* Esto permitirá el scroll normal */
  animation: backgroundShift 60s ease-in-out infinite; /* Movimiento suave del fondo */
  font-size: 1.2rem; /* Aumentamos el tamaño de fuente general */
}

/* Estilos para los botones */
button {
  background-color: #6A4C93 !important;
  color: white;
  border: none;
  padding: 12px 25px; /* Aumentamos el tamaño de los botones */
  border-radius: 5px;
  cursor: pointer;
  z-index: 1; /* Asegura que el botón esté por encima del fondo */
  font-size: 1.1rem; /* Tamaño de texto más grande en los botones */
}

button:hover {
  opacity: 0.9;
}

/* Estilos para la sección hero */
.hero {
  position: relative;
  text-align: center;
  padding: 370px 20px;
  color: white;
}

.intro h1 {
  font-size: 4rem !important; /* O el tamaño que desees */
  margin: 0;
}


.hero h1 span {
  color: #A389DA !important;
}

.hero h2 {
  font-size: 2.5rem; /* Aumentamos el tamaño de h2 */
}

.hero p {
  font-size: 1.5rem; /* Aumentamos el tamaño del texto */
  line-height: 1.6 !important;
}

.hero button {
  margin: 15px !important;
  font-size: 1.2rem; /* Aumentamos el tamaño de texto en los botones */
}

/* Animación suave de desplazamiento en el fondo */
@keyframes backgroundShift {
  0% {
    background-color: #202124;
  }
  50% {
    background-color: #2A2C34; /* Un ligero cambio de color */
  }
  100% {
    background-color: #202124;
  }
}
</style>
