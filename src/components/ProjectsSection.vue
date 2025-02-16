<template>
    <section id="projects" class="projects">
      <div class="container text-center">
        <h2>Mis proyectos</h2>
        <div class="row">
          <div class="col-md-4" v-for="(project, index) in projects" :key="index">
            <div class="project-card">
              <img :src="project.img" alt="Proyecto">
              <h3>{{ project.title }}</h3>
              <p>{{ project.description }}</p>
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
          { title: "Proyecto 1", description: "Descripción breve", img: "img1.jpg" },
          { title: "Proyecto 2", description: "Descripción breve", img: "img2.jpg" },
          { title: "Proyecto 3", description: "Descripción breve", img: "img3.jpg" }
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
    background: #1E1E1E;
    padding: 20px;
    border-radius: 10px;
  }
  </style>
  