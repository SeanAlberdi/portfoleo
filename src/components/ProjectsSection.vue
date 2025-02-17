<template>
  <section id="projects" class="projects">
    <div class="container text-center">
      <h2>Mis proyectos</h2>
      <div class="row">
        <div class="col-md-4" v-for="(project, index) in projects" :key="index">
          <div class="project-card">
            <img :src="project.img" alt="Proyecto" class="project-img" />
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <div class="tech-stack">
              <span v-for="(tech, idx) in project.technologies" :key="idx" class="tech-icon">
                <i :class="tech.icon"></i> <!-- Íconos de Font Awesome -->
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Web Stock y Citas Peluqueria",
          description: "Proyecto de página web para el departamento de Imagen Personal",
          img: "/img1.png",
          technologies: [
            { name: "HTML", icon: "fab fa-html5" },
            { name: "CSS", icon: "fab fa-css3-alt" },
            { name: "JavaScript", icon: "fab fa-js" },
            { name: "Vue.js", icon: "fab fa-vuejs" },
            { name: "Sass", icon: "fa-brands fa-sass" },
            { name: "Bootstrap", icon: "fa-brands fa-bootstrap" },
            { name: "PHP", icon: "fa-brands fa-php" },
            { name: "Laravel", icon: "fa-brands fa-laravel" },
            { name: "Docker", icon: "fa-brands fa-docker" }
          ]
        },
        {
          title: "Portafolio v1",
          description: "Mi primer portafolio realizado solo con Bootstrap",
          img: "/img2.png",
          technologies: [
            { name: "Vue.js", icon: "fab fa-vuejs" },
            { name: "HTML", icon: "fab fa-html5" },
            { name: "CSS", icon: "fab fa-css3-alt" },
            { name: "Bootstrap", icon: "fa-brands fa-bootstrap" }
          ]
        },
        {
          title: "Web Gestion de Materiales del Centro",
          description: "Web para la gestion de equipos informaticos y aulas del centro",
          img: "/img3.png",
          technologies: [
            { name: "PHP", icon: "fa-brands fa-php" },
            { name: "JavaScript", icon: "fab fa-js" },
            { name: "HTML", icon: "fab fa-html5" },
            { name: "CSS", icon: "fab fa-css3-alt" },
            { name: "Bootstrap", icon: "fa-brands fa-bootstrap" },
            { name: "Docker", icon: "fa-brands fa-docker" }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
.projects {
  color: white;
  padding: 50px;
}

.project-card {
  background: #1e1e1e;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  overflow: hidden;
}

.project-img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px;
  margin-bottom: 15px;
}

.project-card h3,
.project-card p {
  margin: 10px 0;
}

.tech-stack {
  display: flex;
  justify-content: center;
  flex-wrap: wrap; /* Esto hace que los íconos se acomoden en múltiples líneas si es necesario */
  gap: 15px;
  margin-top: 15px;
}

.tech-icon {
  font-size: 2rem;
  color: #A389DA; /* Color para los íconos */
}

.tech-icon i {
  transition: transform 0.3s ease;
}

.tech-icon i:hover {
  transform: scale(1.2); /* Efecto de hover */
}
</style>
