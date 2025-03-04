<template>
    <v-container class="skills-section">
      <h2 class="display-1 font-weight-bold mb-6 text-center">Mis Habilidades</h2>
      <v-row>
        <!-- Barra de progreso para cada habilidad -->
        <v-col v-for="(skill, index) in skills" :key="index" cols="12" md="6">
          <div class="skill-item">
            <div class="skill-info">
              <span class="skill-name">{{ skill.name }}</span>
              <span class="skill-percent">{{ skill.percent }}%</span>
            </div>
            <v-progress-linear
              :value="skill.percent"
              height="10"
              :color="getProgressColor(skill.percent)"
              rounded
            ></v-progress-linear>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script setup>
  // Lista de habilidades
  const skills = [
    { name: 'Vue.js', percent: 90 },
    { name: 'JavaScript', percent: 85 },
    { name: 'HTML/CSS', percent: 95 },
    { name: 'Node.js', percent: 80 },
    { name: 'Vuetify', percent: 88 },
    { name: 'Git', percent: 75 },
  ];
  
  // Función para obtener el color de la barra de progreso según el porcentaje
  const getProgressColor = (percent) => {
    if (percent >= 90) return 'success'; // Verde
    if (percent >= 70) return 'primary'; // Azul
    return 'error'; // Rojo
  };
  </script>
  
  <style scoped>
  .skills-section {
    padding: 80px 0;
  }
  
  .skill-item {
    margin-bottom: 20px;
  }
  
  .skill-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 8px;
  }
  
  .skill-name {
    font-size: 1.1rem;
    font-weight: 500;
    color: var(--v-primary-base); /* Color dinámico según el tema */
  }
  
  .skill-percent {
    font-size: 1rem;
    font-weight: 400;
    color: var(--v-secondary-base); /* Color dinámico según el tema */
  }
  </style>