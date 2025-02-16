<template>
  <section class="hero">
    <h1>Hola,</h1><h2>👋</h2><h1> soy <span>Seán Alberdi</span></h1>
    <p>Software Developer.</p>
    <button @click="$emit('scrollToContact')">Contáctame</button>
    <button @click="downloadCV">📥 Descargar CV</button>
  </section>
</template>
  
  <style scoped lang="scss">
  .hero {
    text-align: center;
    padding: 100px 20px;
    color: white;
    h1 span { color: #A389DA; }
  }
  </style>
  