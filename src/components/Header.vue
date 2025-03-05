<template>
    <v-app>
      <!-- Barra de navegación fija -->
      <v-app-bar app color="black" elevate-on-scroll flat style="position: fixed;">
        <v-container class="d-flex align-center">
          <v-toolbar-title class="font-weight-bold">
            ⚡ Alan Robledo
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </v-container>
      </v-app-bar>
  
      <!-- Sección Parallax -->
      <v-parallax src="https://i.ibb.co/Cp2V69Qs/dark-space-wallpaper-2880x900.jpg" height="100vh">
        <v-container
          fill-height
          class="text-center d-flex flex-column align-center justify-end pb-14"
        >
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
          <h1 class="text-h3 font-weight-bold mb-4">
           UI designer & web developer <br />
            <span class="text-primary">Thinking a new world</span>
          </h1>
          <p class="text-subtitle-1">
             Follow my work or contact me<br />
          </p>
          <div class="mt-5">
            <v-btn href="https://github.com/tu-usuario" target="_blank" color="white" outlined class="mr-4"><v-icon left>mdi-github</v-icon>GitHub</v-btn>

        <!-- Botón de Contacto -->
        <v-btn href="mailto:tu-email@example.com"color="white" outlined>
          <v-icon left>mdi-email</v-icon>Contact me</v-btn>
          

          
          </div>
        </v-container>
      </v-parallax>
    </v-app>
  </template>
  
  <script>
  export default {
    name: 'Header',
  };
  </script>
  
  <style scoped>
  .text-primary {
    color: #f88d00 !important; /* Ajuste de color según la imagen */
  }
  
  .v-btn {
    font-size: 18px;
    font-weight: normal;
    text-transform: none;
    padding: 1px 50px;
  }

 
  </style>
  