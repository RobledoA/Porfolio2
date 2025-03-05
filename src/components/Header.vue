<template>
  <v-app>
    <!-- Barra de navegación fija -->
    <v-app-bar app color="black" elevate-on-scroll flat style="position: fixed;">
      <v-container class="d-flex align-center">
        <v-toolbar-title class="font-weight-bold">
          ⚡ Alan Robledo
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </v-container>
    </v-app-bar>

    <!-- Menú de navegación móvil -->
    <v-navigation-drawer v-model="drawer" app temporary>
      <v-list>
        <v-list-item link>
          <v-list-item-title>Inicio</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-title>Proyectos</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-title>Contacto</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- Sección Parallax -->
    <v-parallax src="https://i.ibb.co/Cp2V69Qs/dark-space-wallpaper-2880x900.jpg" height="100vh">
      <br>
      <br>
      br
      <v-container
        fill-height
        class="text-center d-flex flex-column align-center justify-end pb-14"
      >
        <h1 class="text-h4 text-md-h3 font-weight-bold mb-4">
          UI designer & web developer <br />
          <span class="text-primary">Thinking a new world</span>
        </h1>
        <p class="text-subtitle-1 text-center">
          Follow my work or contact me<br />
        </p>
        <div class="mt-5 d-flex flex-column flex-md-row">
          <v-btn
            href="https://github.com/tu-usuario"
            target="_blank"
            color="white"
            outlined
            class="mb-4 mb-md-0 mr-md-4"
          >
            <v-icon left>mdi-github</v-icon>GitHub
          </v-btn>
          <v-btn
            href="mailto:tu-email@example.com"
            color="white"
            outlined
          >
            <v-icon left>mdi-email</v-icon>Contact me
          </v-btn>
        </div>
      </v-container>
    </v-parallax>
  </v-app>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      drawer: false, // Controla la visibilidad del menú móvil
    };
  },
};
</script>

<style scoped>
.text-primary {
  color: #f88d00 !important; /* Ajuste de color según la imagen */
}

.v-btn {
  font-size: 16px;
  font-weight: normal;
  text-transform: none;
  padding: 8px 24px;
}

/* Ajustes para móviles */
@media (max-width: 600px) {
  h1 {
    font-size: 1.75rem !important; /* Tamaño de fuente más pequeño para móviles */
  }

  .v-btn {
    width: 100%; /* Botones de ancho completo en móviles */
    margin-bottom: 8px; /* Espaciado entre botones */
  }
}
</style>