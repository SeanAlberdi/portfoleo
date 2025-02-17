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
  background: linear-gradient(45deg, #202124, #2A2C34);
  background-size: 200% 200%;
  animation: gradientShift 10s ease-in-out infinite;
  color: white;
  margin: 0;
  font-family: 'Arial', sans-serif;
  position: relative;
  overflow-x: hidden;
  font-size: 1.2rem;
}

section {
  position: relative;
  z-index: 1;
}

button {
  background-color: #6A4C93 !important;
  color: white;
  border: none;
  padding: 12px 25px;
  border-radius: 5px;
  cursor: pointer;
  z-index: 1;
  font-size: 1.1rem;
}

button:hover {
  opacity: 0.9;
}

.hero {
  position: relative;
  text-align: center;
  padding: 370px 20px;
  color: white;
}

.intro h1 {
  font-size: 4rem !important;
  margin: 0;
}

.hero h1 span {
  color: #A389DA !important;
}

.hero h2 {
  font-size: 2.5rem;
}

.hero p {
  font-size: 1.5rem;
  line-height: 1.6 !important;
}

.hero button {
  margin: 15px !important;
  font-size: 1.2rem;
}

@keyframes gradientShift {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}

/* Añadiendo líneas estéticas */
body::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" width="800" height="600" viewBox="0 0 800 600"%3E%3Cpath fill="none" stroke="%23A389DA" stroke-width="2" d="M0 50 C 150 100, 200 200, 400 200 S 700 300, 800 500" /%3E%3C/svg%3E') repeat;
  z-index: 0;
  /* Esto coloca las líneas detrás del contenido */
  pointer-events: none;
}
</style>