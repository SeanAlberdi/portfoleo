<template>
  <section id="about" class="about">
    <div class="container">
      <div class="about-content">
        <!-- Contenedor del Título y Descripción -->
        <div class="left-content">
          <h2 class="title">Sobre mí</h2>
          <p class="description">
            Soy un desarrollador Full Stack con una sólida formación en redes y sistemas gracias a mi grado medio, y
            especializado en desarrollo de aplicaciones web con mi grado superior. Me apasiona la tecnología y disfruto
            creando soluciones eficientes y escalables tanto en el frontend como en el backend.
    
            Siempre estoy en busca de nuevos desafíos y oportunidades para seguir aprendiendo y mejorando mis habilidades.
            🚀
          </p>
        </div>

        <!-- Tecnologías alineadas a la derecha -->
        <div class="tech-stack">
          <h3>Tecnologías que uso</h3>
          <ul>
            <li><i class="fab fa-html5"></i> HTML5</li>
            <li><i class="fab fa-css3-alt"></i> CSS3</li>
            <li><i class="fab fa-js"></i> JavaScript</li>
            <li><i class="fab fa-vuejs"></i> Vue.js</li>
            <li><i class="fab fa-bootstrap"></i> Bootstrap</li>
            <li><i class="fab fa-sass"></i> Sass</li>
            <li><i class="fab fa-php"></i> PHP</li>
            <li><i class="fab fa-laravel"></i> Laravel</li>
            <li><i class="fab fa-docker"></i> Docker</li>
            <li><i class="fab fa-aws"></i> AWS</li>
            <li><i class="fab fa-figma"></i> Figma</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    // Aquí pueden ir los métodos, si es necesario en el futuro
  }
};
</script>

<style scoped lang="scss">
.about {
  padding: 50px;
  color: white;
}

.title {
  font-size: 2.5rem; /* Aumentamos el tamaño del título */
  font-weight: bold; /* Ponemos el título en negrita */
  margin-bottom: 20px;
  position: relative; /* Para agregar una línea debajo */
}

.title::after {
  content: "";
  display: block;
  height: 2px;
  background-color: #A389DA; /* Color de la línea */
  width: 50px;
  margin-top: 10px;
}

.about-content {
  display: flex;
  justify-content: space-between; /* Alinea los elementos a los lados */
  align-items: flex-start;
}

.left-content {
  max-width: 60%; /* Limitar el ancho de la parte izquierda */
}

.description {
  font-size: 1.25rem; /* Tamaño adecuado para el texto */
  line-height: 1.6;
  text-align: left; /* Aseguramos que el texto esté alineado a la izquierda */
  max-width: 600px; /* Limitar el ancho para mejor legibilidad */
  margin: 0; /* Alineamos el párrafo a la izquierda */
  padding-bottom: 20px;
}

.tech-stack {
  background-color: #333;
  border-radius: 10px;
  padding: 20px;
  width: 300px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  position: relative;
}

.tech-stack h3 {
  font-size: 1.75rem;
  margin-bottom: 20px;
  text-align: left; /* Alineamos el título de las tecnologías a la izquierda */
  position: relative; /* Para agregar una línea abajo del título */
}

.tech-stack h3::after {
  content: "";
  display: block;
  height: 1px;
  background-color: #A389DA;
  width: 30px;
  margin-top: 8px;
}

.tech-stack ul {
  list-style-type: none;
  padding: 0;
}

.tech-stack li {
  font-size: 1.2rem;
  color: #A389DA;
  margin-bottom: 8px;
  display: flex;
  align-items: center;
}

.tech-stack li i {
  margin-right: 10px; /* Espacio entre el icono y el texto */
  font-size: 1.5rem;
}
</style>
