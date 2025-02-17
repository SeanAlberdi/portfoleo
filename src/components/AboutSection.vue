<template>
  <section id="about" class="about">
    <div class="container text-center">
      <h2 class="title">Sobre mí</h2>
      <p class="description">
        Soy un desarrollador Full Stack con una sólida formación en redes y sistemas gracias a mi grado medio, y
        especializado en desarrollo de aplicaciones web con mi grado superior. Me apasiona la tecnología y disfruto
        creando soluciones eficientes y escalables tanto en el frontend como en el backend.

        Siempre estoy en busca de nuevos desafíos y oportunidades para seguir aprendiendo y mejorando mis habilidades.
        🚀
      </p>
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
}

.description {
  font-size: 1.25rem; /* Tamaño adecuado para el texto */
  line-height: 1.6;
  text-align: center; /* Centramos el texto */
  max-width: 800px; /* Limitar el ancho máximo para mejor legibilidad */
  margin: 0 auto; /* Centrar el párrafo */
}
</style>