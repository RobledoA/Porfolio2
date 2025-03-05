<template>
    <v-container class="projects-section">
      <h2 class="display-1 font-weight-bold mb-6 text-center" style="font-family: 'Playfair Display', serif;">Mis Proyectos</h2>
      <v-row>
        <!-- Tarjeta de proyecto -->
        <v-col v-for="(project, index) in projects" :key="index" cols="12" md="6" lg="4">
          <v-card class="project-card">
            <!-- Imagen del proyecto -->
            <v-img :src="project.image" height="200" class="project-image"></v-img>
  
            <!-- Contenido de la tarjeta -->
            <v-card-text>
              <h3 class="title font-weight-bold mb-2">{{ project.title }}</h3>
              <p class="body-1 mb-4">{{ project.description }}</p>
  
              <!-- Barra de progreso -->
              <v-progress-linear
                :value="project.progress"
                height="10"
                :color="getProgressColor(project.progress)"
                class="mb-4"
              ></v-progress-linear>
  
              <!-- Botón para ver el proyecto -->
              <v-btn
                :href="project.link"
                target="_blank"
                color="primary"
                block
                outlined
              >
                <v-icon left>mdi-open-in-new</v-icon>
                Ver Proyecto
              </v-btn>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'Projects',
    data() {
      return {
        // Lista de proyectos
        projects: [
          {
            title: 'Ey-Commerce',
            description: 'Una aplicación web moderna construida con Vue.js y Vuetify. Es una tienda online en desarrollo',
            image: 'https://i.ibb.co/NdxzFLHz/Screenshot-2025-03-04-231728.png',
            link: 'https://eycommerce2.netlify.app/',
            progress: 80, // Porcentaje de progreso
          },
          {
            title: 'Musik',
            description: 'Aplicación de músicos para músicos. La idea es conectar a la comunidad haciendo más fácil el trabajo de los músicos',
            image: 'https://i.ibb.co/TM7S86h8/Screenshot-2025-03-04-231936.png',
            link: 'https://www.behance.net/gallery/219435429/Musik-(-project-preview)',
            progress: 50,
          },
          {
            title: 'Proyecto 3',
            description: 'Una plataforma de comercio electrónico con integración de pagos en línea.',
            image: 'https://via.placeholder.com/400x200',
            link: 'https://proyecto3.com',
            progress: 100,
          },
        ],
      };
    },
    methods: {
      // Método para obtener el color de la barra de progreso según el porcentaje
      getProgressColor(progress) {
        if (progress >= 100) return 'success';
        if (progress >= 50) return 'primary';
        return 'error';
      },
    },
  };
  </script>
  
  <style scoped>
  .projects-section {
    padding: 80px 0;
  }
  
  .project-card {
    border-radius: 10px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  }
  
  .project-image {
    border-bottom: 1px solid #e0e0e0;
  }
  
  .title {
    font-size: 1.5rem;
    color: #bbbbbb;
  }
  
  .body-1 {
    font-size: 1rem;
    color: #d1d1d1;
    line-height: 1.6;
  }
  </style>