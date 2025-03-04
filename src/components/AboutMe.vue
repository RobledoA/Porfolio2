<template>
    <v-container class="about-me-section">
      <v-row align="center">
        <!-- Columna de la imagen -->
        <v-col cols="12" md="6" class="text-center">
          <v-avatar size="300" class="profile-image">
            <v-img src="D:\Vue\Portfolio\src\assets\profilephoto.jpg" alt="Tu Nombre"></v-img>
          </v-avatar>
        </v-col>
  
        <!-- Columna del texto -->
        <v-col cols="12" md="6">
          <h2 class="display-1 font-weight-bold mb-4" style="font-family: 'Playfair Display', serif;">Sobre Mí</h2>
          <p class="body-1 font-weight-regular" style="font-family: 'Raleway', sans-serif;">
            ¡Hola! Soy Alan Robledo, un apasionado desarrollador web con experiencia en la creación de aplicaciones modernas y escalables. Me especializo en tecnologías como Vue.js, Vuetify, Node.js y más. Disfruto transformar ideas en soluciones digitales que impacten positivamente a los usuarios.
          </p>
          <p class="body-1 font-weight-regular" style="font-family: 'Raleway', sans-serif;">
            Fuera del trabajo, me encanta aprender nuevas tecnologías, contribuir a proyectos de código abierto y disfrutar del aire libre. Siempre estoy buscando nuevos desafíos y oportunidades para crecer profesionalmente.
          </p>
          <v-btn href="mailto:tu-email@example.com"color="white" outlined>
            <v-icon left>mdi-email</v-icon>Curriculum Vitae</v-btn>
        </v-col>
        
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'AboutMe',
  };
  </script>
  
  <style scoped>
  .about-me-section {
    padding: 80px 0;
  }
  
  .profile-image {
    border: 5px solid #ffffff;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .display-1 {
    font-size: 2.5rem;
    color: #c2c2c2;
    margin-bottom: 20px;
  }
  
  .body-1 {
    font-size: 1.1rem;
    color: #bebebe;
    line-height: 1.8;
    margin-bottom: 20px;
  }
  
  /* Estilos responsivos */
  @media (max-width: 960px) {
    .profile-image {
      margin-bottom: 30px;
    }
  }
  </style>