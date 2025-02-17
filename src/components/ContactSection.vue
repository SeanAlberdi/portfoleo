<template>
  <section id="contact" class="contact">
    <div class="container">
      <div class="contact-content">
        <!-- Formulario -->
        <div class="form-container">
          <h2 class="title">Contáctame</h2>
          <hr class="line"> <!-- Línea debajo del título -->
          <form @submit.prevent="sendEmail">
            <div class="form-group">
              <label for="name">Tu nombre</label>
              <input type="text" id="name" v-model="form.name" required />
            </div>
            <div class="form-group">
              <label for="email">Tu email</label>
              <input type="email" id="email" v-model="form.email" required />
            </div>
            <div class="form-group">
              <label for="subject">Asunto</label>
              <input type="text" id="subject" v-model="form.subject" required />
            </div>
            <div class="form-group">
              <label for="message">Mensaje</label>
              <textarea id="message" v-model="form.message" required></textarea>
            </div>
            <button type="submit">Enviar</button>
          </form>
        </div>

        <!-- Texto con datos estáticos -->
        <div class="text-container">
          <h3>Contactame</h3>
          <div class="contact-details">
            <p><strong>Email:</strong> alberdisean@gmail.com</p>
            <p><strong>Teléfono:</strong> +34 123 456 789</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import emailjs from "emailjs-com"; // Asegúrate de importar EmailJS

export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        subject: "",
        message: "",
      }
    };
  },
  methods: {
    async sendEmail() {
      const emailData = {
        name: this.form.name,
        email: this.form.email,
        subject: this.form.subject,
        message: this.form.message,
      };

      try {
        // Enviar el correo usando EmailJS
        await emailjs.send("service_47tx38k", "template_6pllm1o", emailData, "YAZs4yAiPL-MhcDKr");
        alert("¡Correo enviado con éxito!");
        // Limpia el formulario después de enviar
        this.form = {
          name: "",
          email: "",
          subject: "",
          message: "",
        };
      } catch (error) {
        alert("Hubo un error al enviar el correo.");
      }
    }
  }
};
</script>

<style scoped lang="scss">
.contact {
  padding: 50px;
  color: white;
}

.contact-content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.form-container {
  background-color: #333;
  padding: 20px;
  border-radius: 10px;
  width: 50%;
}

.title {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  font-size: 1.2rem;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  background-color: #6A4C93;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  opacity: 0.9;
}

.text-container {
  max-width: 35%;
}

.text-container h3 {
  font-size: 3rem;  /* Tamaño grande para el título */
  font-weight: bold;
  color: #A389DA;
}

.contact-details p {
  font-size: 1.2rem;
  margin: 10px 0;
}

/* Línea estética debajo del título */
.line {
  border: 0;
  height: 2px;
  background: #A389DA;
  margin: 20px 0;
}
</style>
