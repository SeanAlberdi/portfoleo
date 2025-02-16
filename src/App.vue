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
  downloadCV() {
      const link = document.createElement('a');
      link.href = '/cv.pdf';
      link.download = 'cv.pdf';
      link.click();
    }
};
</script>

<style>
body {
  background-color: #202124 !important;
  color: white;
  margin: 0;
  font-family: 'Arial', sans-serif;
}

button {
  background-color: #6A4C93 !important;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  opacity: 0.9;
}
</style>